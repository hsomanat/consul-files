node {
        stage('build') {
                String repo_name="consul-files"
	        String repo_loc = "$WORKSPACE/${repo_name}"
		if (fileExists(repo_loc)) {
			println repo_loc + " already exists, do not clone"
		} else {
			println "Setup local ${repo_name} repo"
			sh """
				set +x
				git clone 'https://github.com/hsomanat/consul-files.git' $repo_loc
                        """  
                }
                   def contents = readFile $repo_loc/zones.yaml
                   sh "curl  --request PUT --data contents http://127.0.0.1:8500/v1/kv/foo1"
          
        }
 
}

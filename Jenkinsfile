node {
        stage('build') {
                
			
			sh """
				set +x
				git clone 'https://github.com/hsomanat/consul-files.git' /Users/Shared/Jenkins/Home/workspace/consul-test1
                        """  
                
                   def contents = readFile /Users/Shared/Jenkins/Home/workspace/consul-test1/zones.yaml
                   sh "curl  --request PUT --data contents http://127.0.0.1:8500/v1/kv/foo1"
          
        }
 
}

node {
        stage('build') {
            
                env.WORKSPACE = pwd()
                def contents = readFile "${env.WORKSPACE}/zones.yaml"
                sh "curl  --request PUT --data contents http://127.0.0.1:8500/v1/kv/foo1"
          
        }
 
}

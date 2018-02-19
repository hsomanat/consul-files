node {
        stage('build') {
                
                   def contents = readFile "/Users/Shared/Jenkins/Home/workspace/consul-test1/zones.yaml"
                   echo contents
                sh "curl  --request PUT --data '$contents' http://127.0.0.1:8500/v1/kv/foo1"
          
        }
 
}


 
pipeline {
    /* specify nodes for executing */
    agent {
        label 'master'
    }
 
    stages {
        /* checkout repo */
        stage('Checkout SCM') {
            steps {
                checkout([
                 $class: 'GitSCM',
                 branches: [[name: 'master']],//scm.branches
                 userRemoteConfigs: [[
                    url: 'git@github.com:wshihadeh/rabbitmq_client.git',
                    
                 ]]
                ])
            }
        }
         stage('Do the deployment') {
            steps {
                echo ">> Run deploy applications test"
            }
        }
    }
 
    /* Cleanup workspace */
    post {
       always {
           deleteDir()
       }
   }
}


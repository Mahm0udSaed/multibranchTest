properties([pipelineTriggers([githubPush()])])
 
pipeline {
    /* specify nodes for executing */
    agent {
        label 'github-ci'
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

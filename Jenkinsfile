pipeline {
    agent any 
        environment {
            USERNAME =  dummy_creds('username')
        }
        stages {
            stage ('Deploy') {
                steps {
                    echo 'username is ${USERNAME}'
                }
            }
        }
    
    post {
        always {
            echo 'This will always run'
        }
        success {
            echo 'This is SUCCESS'
        }
        failure {
            echo 'This is failure'
        }
        unstable {
            echo 'This will run only if the run was marked as unstable'
        }
        changed {
            echo 'This will run only if the state of the Pipeline has changed'
            echo 'For example, if the Pipeline was previously failing but is now successful'
        }               
    }
}

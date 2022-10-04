pipeline {
    agent any 
        environment {
            DUMMY_CREDS =  credentials('dummy_creds')
        }
        stages {
            stage ('Deploy') {
                steps {
                    echo 'username is ${DUMMY_CREDS_USR} password is ${DUMMY_CREDS_PSW}'
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

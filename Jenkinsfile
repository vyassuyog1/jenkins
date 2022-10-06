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
            junit 'build/reports/**/*.xml'
        }
    }
}

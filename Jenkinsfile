pipeline {
    agent any 
        environment {
            DUMMY_CREDS =  credentials('dummy creds')
        }
        stages {
            stage ('Deploy') {
                steps {
                    echo 'xyz'
                }
            }
        }
    
    post {
        always {
            echo 'This will always run'
        }
    }
}

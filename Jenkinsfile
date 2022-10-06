pipeline {
    agent any 
        environment {
            DUMMY_CREDS =  credentials('dummy creds')
        }
        stages {
            stage ('Deploy') {
                steps {
                    bat 'name.bat'
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

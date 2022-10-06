pipeline {
    agent any 
        environment {
            DUMMY_CREDS =  credentials('dummy creds')
        }
        stages {
            stage ('Deploy') {
                steps {
                    bat 'conda activate 8x81'
                    bat 'python test.py'
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

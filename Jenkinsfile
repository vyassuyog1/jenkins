pipeline {
    agent any 
        environment {
            DUMMY_CREDS =  credentials('dummy creds')
        }
        stages {
            stage ('Deploy') {
                steps {
                    bat 'pytest test.py --junitxml=build/reports/demo/result.xml'
                   
                }
            }
        }
    
    post {
        always {
            echo 'This will always run'
            archiveArtifacts artifacts: 'build/*.jar', fingerprint: true
            junit 'build/reports/**/*.xml'
            
        }
    }
}

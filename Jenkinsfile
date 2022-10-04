pipeline {
    agent any 
        stages {
            stage ('Deploy') {
                steps {
                    retry (3) {
                        bat 'name.bat'
                    }
                    timeout (time: 3, unit: 'MINUTES') {
                        bat 'next.bat'
                    }
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

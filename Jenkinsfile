pipeline {
    agent any {
        stage ('Deploy') {
            steps {
                retry (3) {
                    bat './name.sh'
                }
                timeout (time: 3, unit: 'MINUTES') {
                    bat './next.sh'
                }
            }
        }   
    }
}

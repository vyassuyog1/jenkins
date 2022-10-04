pipeline {
    agent any {
        steps ('Deploy') {
            retry (3) {
                bat './name.sh'
            }
            timeout (time: 3, unit: 'MINUTES') {
                bat './next.sh'
            }
        }
    }
}

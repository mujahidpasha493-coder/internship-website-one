pipeline {
    agent any

    stages {
        stage('Deploy Website One') {
            steps {
                sh '''
                    set -e
                    cp index.html style.css /var/www/website-one/
                '''
            }
        }
    }
}

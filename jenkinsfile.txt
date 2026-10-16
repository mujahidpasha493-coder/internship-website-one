pipeline {
    agent any

    stages {
        stage('Deploy Website One') {
            steps {
                sh '''
                    set -e
                    sudo cp -r ./* /var/www/website-one/
                    sudo chown -R jenkins:webdeploy /var/www/website-one
                    sudo chmod -R 775 /var/www/website-one
                '''
            }
        }
    }
}

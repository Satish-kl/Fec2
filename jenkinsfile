pipeline {

    agent any

    stages {

        stage('Clone Repository') {

            steps {

                git branch: 'main',
                url: 'https://github.com/Satish-kl/Fec2.git'

            }

        }

        stage('Deploy Website') {

            steps {

                sh '''
                sudo rm -rf /var/www/html/*
                sudo cp -r * /var/www/html/
                sudo systemctl restart nginx
                '''

            }

        }

    }

}

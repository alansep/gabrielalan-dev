pipeline {
    agent any

    stages {
        stage ('Preparando compilação'){
            steps {
                script {
                    sh 'npm i --legacy-peer-deps'
                }
            }
        }
        stage ('Compilando SPA'){
            steps {
                script {
                    sh 'ng build --base-href .'
                }
            }
        }
        stage ('Publicando projeto'){
            steps {
                script {
                    sh 'cp -r ./dist/gabrielalan-dev/* /var/www/html/'
                }
            }
        }
    }
}
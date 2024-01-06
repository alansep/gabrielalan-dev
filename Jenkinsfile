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
        stage ('Where am I?'){
            steps {
                script {
                    sh 'pwd'
                }
            }
        }
         stage ('Who am I?'){
            steps {
                script {
                    sh 'whoami'
                }
            }
        }
        stage ('Publicando projeto'){
            steps {
                script {
                    sh 'cp ./dist/gabrielalan-dev/* /home/ubuntu/links/deployment/'
                }
            }
        }
    }
}
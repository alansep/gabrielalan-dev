pipeline {
    agent any

    stages {
        stage ('Where am I?'){
            steps {
                script {
                    sh 'pwd'
                }
            }
        }
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
                    sh 'cp /home/ubuntu/links/compilados/gabrielalan.dev/* /home/ubuntu/links/producao/gabrielalan.dev/'
                }
            }
        }
    }
}
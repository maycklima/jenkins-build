pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                // Esse passo é necessário para clonar o repositório
                checkout scm
            }
        }
        stage('Build Docker Image') {
            steps {
                script {
                    sh 'docker build -t jenkins-build .'
                }
            }
        }
        stage('Clone Repo') {
        steps {
            sh 'git clone https://github.com/maycklima/izzydata-vendas.git .'
            }
        }
    }
}

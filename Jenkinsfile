pipeline {
    agent any

    options {
        buildDiscarder(logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '', daysToKeepStr: '', numToKeepStr: '1'))
    }

    environment {
        PATH = "${tool 'Node.js'}/bin:${env.PATH}"
    }

    stages {
        stage('Clone do Repositório Nodegoat') {
            steps {
                script {
                    git 'https://github.com/Giovanellucas/NodeGoat-master.git'
                }
            }
        }

        stage('Configuração do Repositório no Jenkins') {
            steps {
                withCredentials([git(credentialsId: 'seu-id-de-credencial-git', url: 'https://github.com/Giovanellucas/NodeGoat-master.git')]) {
                    sh 'npm install'
                }
            }
        }

        stage('Criação da Stage de Testes') {
            steps {
                sh 'npm test'
            }
        }

        stage('Execução e Monitoramento') {
            steps {
            }
        }

        stage('Análise de Logs') {
            steps {
            }
        }
    }

    post {
        always {
        }
    }
}

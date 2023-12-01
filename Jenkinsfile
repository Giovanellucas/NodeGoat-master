pipeline {
    agent any

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
                script {
                    withCredentials([git(credentialsId: 'seu-id-de-credencial-git', url: 'https://github.com/Giovanellucas/NodeGoat-master.git')]) {
                        sh 'npm install'
                    }
                }
            }
        }

        stage('Criação da Stage de Testes') {
            steps {
                script {
                    sh 'npm test'
                }
            }
        }

        stage('Execução e Monitoramento') {
            steps {
                script {
                 
                }
            }
        }

        stage('Análise de Logs') {
            steps {
                script {
                  
                }
            }
        }
    }

    post {
        always {
        }
    }
}

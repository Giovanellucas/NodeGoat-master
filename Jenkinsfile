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
        }pipeline {
    agent any

    options {
        buildDiscarder(logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '', daysToKeepStr: '', numToKeepStr: '1'))
    }

    environment {
        // Definir a variável de ambiente PATH para incluir o Node.js
        PATH = "${tool 'Node.js'}/bin:${env.PATH}"
    }

    stages {
        stage('Clone do Repositório Nodegoat') {
            steps {
                // Clonar o repositório Nodegoat
                script {
                    git 'https://github.com/Giovanellucas/NodeGoat-master.git'
                }
            }
        }

        stage('Configuração do Repositório no Jenkins') {
            steps {
                // Configurar o repositório no Jenkins
                // Certifique-se de ter as credenciais do Git configuradas no Jenkins
                // e ajuste conforme necessário
                withCredentials([git(credentialsId: 'seu-id-de-credencial-git', url: 'https://github.com/Giovanellucas/NodeGoat-master.git')]) {
                    sh 'npm install'
                }
            }
        }

        stage('Criação da Stage de Testes') {
            steps {
                // Adicionar uma stage no Jenkinsfile do Nodegoat para executar os testes
                // Certifique-se de que o Node.js e o npm estão instalados no servidor do Jenkins
                // Adicione os comandos necessários para inicializar a aplicação e executar os testes
                sh 'npm test'
            }
        }

        stage('Execução e Monitoramento') {
            steps {
                // Adicione comandos relevantes para a execução e monitoramento, se necessário
                script {
                    // Exemplo de comando, ajuste conforme necessário
                    echo 'Executando e monitorando...'
                }
            }
        }

        stage('Análise de Logs') {
            steps {
                // Adicione comandos para análise de logs, se necessário
                script {
                    // Exemplo de comando, ajuste conforme necessário
                    echo 'Analisando logs...'
                }
            }
        }
    }

    post {
        always {
            // Realize qualquer ação de limpeza necessária aqui
            script {
                // Exemplo de comando, ajuste conforme necessário
                echo 'Ações sempre executadas...'
            }
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

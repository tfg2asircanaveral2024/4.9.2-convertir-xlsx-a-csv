pipeline {
    agent any

    stages {
        stage('Convertir Ficheros') {
            agent {
                label 'agente-pwsh-jnlp'
            }

            steps {
                dir('/var/jenkins_home/workspace-compartido') {
                    pwsh './script-pwsh.ps1'
                }
            }
        }

        stage('Mostrar Ficheros') {
            steps {
                dir('/var/jenkins_home/workspace-compartido') {
                    sh 'ls -Rl'
                }
            }
        }
    }
}
pipeline {
    agent any

    stages {
        stage ('Descargar Repositorio') {
            steps {
                git 'https://github.com/tfg2asircanaveral2024/4.9.2-convertir-xlsx-a-csv.git'
            }
        }

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
pipeline {
    agent any

    stages {
        stage('Convertir Ficheros') {
            agent {
                label 'agente-pwsh-jnlp'
            }

            steps {
                pwsh './script-pwsh.ps1'
                sh 'ls -Rl'
            }
        }

        stage('Mostrar Ficheros') {
            steps {
                sh 'ls -Rl'
            }
        }
    }
}
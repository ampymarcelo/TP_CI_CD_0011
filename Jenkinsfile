pipeline {
    agent any

    stages {

        stage('Récupérer le code') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/ampymarcelo/TP_CI_CD_0011.git'
            }
        }

        stage('Compiler') {
            steps {
                bat 'javac Helloworld.java'
            }
        }

        stage('Tester') {
            steps {
                bat 'java HelloWorld'
            }
        }

        stage('Résultat') {
            steps {
                echo 'Build terminé avec succès !'
            }
        }

    }

    post {
        success {
            echo 'Pipeline réussi !'
        }
        failure {
            echo 'Pipeline échoué !'
        }
    }
}
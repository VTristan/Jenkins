pipeline {
    agent any

    tools {
    // Spécifiez l'installation de Maven configurée dans Jenkins
        maven 'Maven 3.9.6'
    }

    stages {
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Run') {
            steps {
                sh 'java -jar target/app-1.0-SNAPSHOT.jar'
            }
        }

        stage('Deploy') {
            steps {
                echo 'todo'
                // Ajoutez les étapes de déploiement si nécessaire
            }
        }
    }

    post {
        success {
            echo 'Le build a réussi!'
            // Exemple de notification par email
        
        }

        failure {
            // Actions à effectuer en cas d'échec (peut être la notification, le rollback, etc.)
            echo 'Le build a échoué!'
        }
    }
}

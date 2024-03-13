pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
            sh 'mvn clean install'
            }
        }
        stage('Run') {
            steps {
                sh 'java -jar target/app-1.0-SNAPSHOT.jar'
            }
        }
        stage('Deploy') {
            steps {
                //
            }
        }

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
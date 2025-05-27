pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                echo 'Cloning repository...'
                // Git is already checked out via SCM config
            }
        }

        stage('Read Text File') {
            steps {
                echo 'Reading myfile.txt...'
                bat 'type myfile.txt'
            }
        }
    }

    post {
        success {
            echo 'File read successfully.'
        }
        failure {
            echo 'Failed to read the file.'
        }
    }
}

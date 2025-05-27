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
                // Assuming the file is in the repo root
                sh 'cat myfile.txt'
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

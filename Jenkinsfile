pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                echo 'Cloning repository...'
                checkout scm
            }
        }

        stage('Run Script') {
            steps {
                echo 'Running script...'
                sh 'bash script.sh'
            }
        }
    }
}

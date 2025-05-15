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
post {
        always {
            mail to: 'sujishreek2002@gmail.com',
                 subject: "Jenkins Build: ${currentBuild.fullDisplayName}",
                 body: "Build result: ${currentBuild.currentResult}\n\nCheck console output at: ${env.BUILD_URL}"
        }
    }
}

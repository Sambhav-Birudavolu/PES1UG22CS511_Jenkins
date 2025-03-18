pipeline {
    agent any

    stages {
        stage('Clone repository') {
            steps {
                checkout([$class: 'GitSCM', 
                          branches: [[name: '*/main']],
                          userRemoteConfigs: [[url: 'https://github.com/Sambhav-Birudavolu/PES1UG22CS511_Jenkins']]])
            }
        }

        stage('Build') {
            steps {
                build 'PES1UG22CS511-1'
                sh 'g++ 511_program.cpp -o output'
            }
        }

        stage('Test') {
            steps {
                sh 'wwdwdadadad'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed!'
        }

        success {
            echo 'Pipeline completed successfully!'
        }
    }
}

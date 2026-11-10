
pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Building Wizard Almanac...'
                sh 'docker compose build app'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing Wizard Almanac...'
                sh 'docker compose config -q'
                echo 'Docker Compose configuration is valid!'
            }
        }

        stage('Start') {
            steps {
                echo 'Starting Wizard Almanac...'
                sh 'docker compose up -d app'
            }
        }
    }

    post {
        success {
            echo 'Wizard Almanac started successfully!'
        }
        failure {
            echo 'Pipeline failed. Check Console Output.'
        }
    }
}

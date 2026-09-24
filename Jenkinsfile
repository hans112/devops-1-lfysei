pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Building Wizard Almanac...'
                sh 'docker compose build'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing Wizard Almanac...'
                sh 'docker compose config'
            }
        }

        stage('Start') {
            steps {
                echo 'Starting Wizard Almanac...'
                sh 'docker compose up -d'
            }
        }
    }
}
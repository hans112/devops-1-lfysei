pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Building Wizard Almanac and Jenkins...'
                bat 'docker compose build app jenkins'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing Wizard Almanac...'
                bat 'docker compose config'
            }
        }

        stage('Start') {
            steps {
                echo 'Starting Wizard Almanac...'
                bat 'docker compose up -d'
            }
        }
    }
}
pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/ТВОЄ_ІМ’Я/labs_git.git'
            }
        }

        stage('Build') {
            steps {
                bat 'echo Build step completed (placeholder)'
            }
        }

        stage('Test') {
            steps {
                bat 'pytest'
            }
        }

        stage('Delivery') {
            steps {
                bat '''
                if exist "%USERPROFILE%\\cargo" rd /s /q "%USERPROFILE%\\cargo"
                mkdir "%USERPROFILE%\\cargo"
                xcopy /E /I /Y * "%USERPROFILE%\\cargo\\"
                '''
            }
        }
    }
}

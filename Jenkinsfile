pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git git 'https://github.com/odvova/it_product_lifecycle.git'
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

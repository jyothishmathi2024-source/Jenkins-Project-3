pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/jyothishmathi2024-source/Jenkins-Project-3.git'
            }
        }

        stage('Build') {
            steps {
                bat 'C:\\Users\\saaij\\AppData\\Local\\Programs\\Python\\Launcher\\py.exe -m py_compile app.py'
                echo 'Build successful: app.py compiled with no syntax errors'
            }
        }

        stage('Deploy') {
            steps {
                input message: 'Approve deployment to production?', ok: 'Deploy'
                bat 'C:\\Users\\saaij\\AppData\\Local\\Programs\\Python\\Launcher\\py.exe app.py'
            }
        }

    }
}
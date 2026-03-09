pipeline {
    agent any

    stages {

        stage('Install Libraries') {
            steps {
                bat '"C:\\Users\\staff\\AppData\\Local\\Programs\\Python\\Python313\\python.exe" -m pip install -r requirements.txt'
            }
        }

        stage('Convert Notebook') {
            steps {
                bat 'jupyter nbconvert --to script train_model.ipynb'
            }
        }

        stage('Run Training') {
            steps {
                bat '"C:\\Users\\staff\\AppData\\Local\\Programs\\Python\\Python313\\python.exe" train_model.py'
            }
        }

    }
}
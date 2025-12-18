pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/SamrudhiSatpute/B73-jenkins-python-pipeline.git'
            }
        }

        stage('Install Python Dependencies') {
            steps {
                bat 'pip install pytest'
            }
        }

        stage('Run Tests') {
            steps {
                bat '''
                set PYTHONPATH=%WORKSPACE%
                pytest test_calculator.py -q
                '''
            }
        }
    }
}

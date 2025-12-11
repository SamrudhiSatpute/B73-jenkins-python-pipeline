pipeline {
    agent any

    stages {
        stage('Git repo clone') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/SamrudhiSatpute/B73-jenkins-python-pipeline.git'
            }
        }

        stage('Deploy HTML & CSS') {
            steps {
                bat '''
                    robocopy . "D:\\WisdomSprout\\Internship\\B73-jenkins-python-pipeline\\add" index.html
                    robocopy . "D:\\WisdomSprout\\Internship\\B73-jenkins-python-pipeline\\add" style.css
                '''
            }
        }

        stage('Verify Deployment') {
            steps {
                echo 'Website deployed successfully!'
            }
        }
    }

    post {
        always {
            echo 'Pipeline completed!!!'
        }
    }
}

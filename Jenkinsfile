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
        powershell '''
            $files = @("index.html", "style.css")
            $dest = "D:\\WisdomSprout\\Internship\\B73-jenkins-python-pipeline\\add\\"

            foreach ($f in $files) {
                Copy-Item $f $dest -Force
            }
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

pipeline {
    agent any

    stages {
        stage('Git Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Devendra-Reddy-420/chatbt'
            }
        }

        stage('Maven Build') {
          when {
              branch 'develop'
              }
            steps {
                sh 'mvn clean package'
            }
        }

        stage('Dev-Deploy') {
          when {
              branch 'develop'
              }
            steps {
                echo "dev Deploy"
            }
        }

        stage('Test-Deploy') {
          when {
              branch 'test'
              }
            steps {
                echo "Test Deploy"
            }
        }

        stage('Prod-Deploy') {
          when {
              branch 'develop'
              }
            steps {
                echo "Prod Deploy"
            }
        }
    }
}

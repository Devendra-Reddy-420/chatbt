pipeline {
    agent any

    stages {
        stage('Maven Build') {
            steps {
                sh 'mvn clean package'
            }
        }
         stage('Dev Deploy') {
             when{
                 branch "develop"
             }
            steps {
                echo "deploying to dev"
            }
        }
        stage('Test Deploy') {
            when{
                 branch "test"
             }
            steps {
                echo "deploying to test"
            }
        }
        stage('prod Deploy') {
            when{
                 branch "main"
             }
            steps {
                echo "deploying to prod"
            }
        }
    }
}


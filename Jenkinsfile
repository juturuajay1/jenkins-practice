pipeline{
    agent { label 'AGENT-1' }
    environment {
        PROJECT = 'expense'
        COMPONENT = 'BACKEND'
    }
    options {
        disabelConcurrentBuilds()
    }
    stages{
        stage('Build'){
            steps{
                script{
                    sh """
                      echo "Hello, this is build"
                      echo "Project is : $PROJECT"
                    """
                }
            }
        }
        stage('Test'){
            steps{
                script{
                    sh """
                      echo "Hello, this is Test"
                    """
                }
            }
        }
        stage('Deploy'){
            steps{
                script{
                    sh """
                      echo "Hello, this is Deploy"
                    """
                }
            }
        } 
    }
    post {
        always {
            echo 'I will always say Hello again!'
        }
        failure {
            echo 'I will run when pipeline is failed'
        }
        success{
            echo 'I will run when pipeline is success'
        }
    }
} 
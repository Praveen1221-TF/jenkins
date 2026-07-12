pipeline {
    agent {
        node{
            label 'Agent-1'
        }
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing...'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }

    post{
        always{
            echo 'I will always say hello again!'
            cleanWs()
        }
        sucess{
            echo 'I will run if sucess'

        }
        failure{
            echo 'i will run if fail'

        }
    }
}
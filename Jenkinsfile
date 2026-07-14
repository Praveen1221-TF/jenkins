pipeline {
    agent {
        node{
            label 'Agent-1'
        }
    }

    stages {
        stage('Build') {
            steps {
                script{
                    sh "" ""
                        echo "Building"
                    "" ""
                 }
            }
        }

        stage('Test') {
            steps {
                script{
                    sh "" ""
                        echo "Testing"
                    "" ""
                 }
            }
        }

        stage('Deploy') {
            steps {
                script{
                    sh "" ""
                        echo "Deploying"

                    "" ""
                 }
            }
        }
    }

    post{
        always{
            echo 'I will always say hello again!'
            cleanWs()
        }
        success{
            echo 'I will run if sucess'

        }
        failure{
            echo 'i will run if fail'

        }
    }
}
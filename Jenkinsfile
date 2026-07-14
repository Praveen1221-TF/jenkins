pipeline {
    agent {
        node{
            label 'Agent-1'
        }
    }
    environment {
        COURSE = "Jenkins"
    }

    options {
        timeout(time: 10, unit: 'MINUTES') 
        disableConcurrentBuilds()  
    }

    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
        booleanParam(name: 'DEPLOY', defaultValue: false, description: 'Toggle this value')
        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }

    stages {
        stage('Build') {
            steps {
                script{
                    sh """
                        echo "Building"
                        echo $COURSE
                        sleep 10
                        env

                        echo "Hello ${params.PERSON}"
                        echo "Biography: ${params.BIOGRAPHY}"
                        echo "Toggle: ${params.DEPLOY}"
                        echo "Choice: ${params.CHOICE}"
                        echo "Password: ${params.PASSWORD}"
                    """
                }
            }
        }   

    stages {
        stage('Build') {
            steps {
                script{
                    sh '''
                        echo "Building"
                        echo $COURSE
                        sleep 10
                        env
                    '''
                 }
            }
        }

        stage('Test') {
            steps {
                script{
                    sh '''
                        echo "Testing"
                    '''
                 }
            }
        }

        stage('Deploy') {
            steps {
                script{
                    sh '''
                        echo "Deploying"

                    '''
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
        aborted {
            echo 'pipeline is aborted'
        }
    }
}
pipeline {
    agent { node { label 'AGENT-1' } }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh '''
                  ls -ltr
                  pwd
                  echo "hello from github webhook event from jenkins"
                '''
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
    post { 
        always { 
            echo 'I will always run wheather job is success or not'
        }
        success{
            echo 'I will run only when job is success'
        }
        failure{
            echo 'I will run when failure'
        }
    }
}
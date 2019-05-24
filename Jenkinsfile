pipeline {
    agent any
    stages {
        stage('Build') {
            when { not { buildTag() } }
            steps {
                echo 'make package'
            }
        }
        stage('Test') {
            when { not { buildTag() } }
            steps {
                echo 'make check'
            }
        }
        stage('Deploy') {
            when { tag 'deploy-*' }
            steps {
                echo 'Deploying only because this commit is tagged...'
                echo 'make deploy'
            }
        }
    }
}

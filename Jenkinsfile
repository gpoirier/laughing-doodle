pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'make package'
            }
        }
        stage('Test') {
            steps {
                echo 'make check'
            }
        }
        stage('Deploy') {
            when { buildingTag() }
            steps {
                echo 'Deploying only because this commit is tagged...'
                echo 'make deploy'
            }
        }
    }
}

pipeline {
    agent { label 'kubernetes' }
    stages {
        stage('Test') {
            steps {
                timestamps {
                    echo "Testing..."
                }
            }
        }
        stage('Release') {
            steps {
                timestamps {
                    echo "Releasing..."
                }
            }
        }
        stage('Deploy') {
            steps {
                timestamps {
                    echo "Deploying..."
                }
            }
        }
    }
}

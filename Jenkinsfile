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
        stage('CX') {
            when {
                anyOf {
                    branch 'master'
                    branch '*-rc'
                    branch '*-beta'
                }
            }
            steps {
                timestamps {
                    echo "CX deployment..."
                }
            }
        }
        stage('Deploy') {
            when {
                buildingTag()
                tag pattern: "deploy-*"
            }
            steps {
                timestamps {
                    echo "Deploying..."
                    sh 'set'
                }
            }
        }
    }
}

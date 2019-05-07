pipeline {
    agent { label 'kubernetes' }
    stages {
        stage('Clean') {
            steps {
                timestamps {
                    sh "echo Cleaning..."
                }
            }
        }
        stage('Build') {
            steps {
                timestamps {
                    sh "echo Building..."
                }
            }
        }
        stage('Unit Tests') {
            parallel {
                stage('Running tests #1') {
                    steps {
                        timestamps {
                            sh "Running tests #1..."
                        }
                    }
                }
                stage('Running tests #2') {
                    steps {
                        timestamps {
                            sh "Running tests #2..."
                        }
                    }
                }
            }
        }
    }
}

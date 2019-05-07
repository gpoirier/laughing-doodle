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
                            sh '''
                              echo "Starting tests #1..."
                              sleep 2
                              echo "Ending tests #1..."
                              exit 1
                            '''
                        }
                    }
                }
                stage('Running tests #2') {
                    steps {
                        timestamps {
                            sh "echo Running tests #2..."
                        }
                    }
                }
            }
        }
    }
}

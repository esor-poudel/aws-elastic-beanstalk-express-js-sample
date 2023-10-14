pipeline {
    agent {
        docker {
            image 'node:16'
            args '-u root' // Optional: Run as root if necessary
        }
    }
    
    stages {
        stage('Set Environment') {
            steps {
                script {
                    // Set the DOCKER_HOST environment variable
                    withEnv(["DOCKER_HOST=tcp://dind:2375"]) {
                        // Inside this block, DOCKER_HOST will be set
                        // for the duration of the stage.
                    }
                }
            }
        }

        stage('Build') {
            steps {
                sh 'npm install --save'
            }
        }

        stage('test') {
            steps {
                echo "Testing the Application ...."
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying ...."
            }
        }
    }
}

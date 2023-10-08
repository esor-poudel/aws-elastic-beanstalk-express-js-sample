pipeline {
    agent {
        docker {
            image 'node:16'
            args '-u root' // Optional: Run as root if necessary
        }
    }
    
    stages {
        stage('Build') {
            steps {
                sh 'npm install --save'
            }
        }

        stage('test'){
            steps{
                echo "Testing the Application ...."
            }
        }

        stage('Deploy'){
            steps{
                echo "Deploying ...."
            }
        }
    }
    
    
}

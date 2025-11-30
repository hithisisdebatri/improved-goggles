pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                echo "Cloning the repository from GitHub: hithisisdebatri/improved-goggles."
                checkout scm 
                echo "Code checked out successfully."
            }
        }
        
        stage('Verify Files') {
            steps {
                echo "Verifying presence of critical HTML file..."
                // NOTE: If your main file is NOT named index.html, change 'index.html' below!
                sh 'ls -l index.html'
                echo "index.html confirmed."
            }
        }
        
        stage('Deploy Staging') {
            steps {
                echo "--- Deployment Simulation Started ---"
                // Placeholder for your actual deployment commands
                sh 'echo "Simulating file transfer to the staging server..." > deployment_log.txt'
                echo "Deployment simulation finished."
            }
        }
    }
    
    post {
        always {
            echo "Pipeline run completed. Check console output for details."
        }
        success {
            echo "SUCCESS: Build finished without errors!"
        }
        failure {
            echo "FAILURE: Review the stage where the error occurred."
        }
    }
}

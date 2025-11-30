pipeline {
    // This tells Jenkins to run the job on any available agent (your Windows machine).
    agent any

    stages {
        
        // Stage 1: Get the source code from GitHub
        stage('Checkout Code') {
            steps {
                echo "Cloning the repository from GitHub: hithisisdebatri/improved-goggles."
                // This step automatically pulls the code from the Git URL set in the Jenkins job configuration.
                checkout scm 
                echo "Code checked out successfully."
            }
        }
        
        // Stage 2: Verify the essential files are present
        stage('Verify Files') {
            steps {
                echo "Verifying presence of critical HTML file..."
                // FIX: We use 'bat' (Windows Batch) instead of 'sh' (Linux Shell)
                // 'dir index.html' is a simple Windows command to confirm the file exists in the workspace.
                bat 'dir index.html' 
                echo "index.html confirmed."
            }
        }
        
        // Stage 3: Deployment Simulation (Placeholder for future deployment steps)
        stage('Deploy Staging') {
            steps {
                echo "--- Deployment Simulation Started ---"
                // FIX: Using 'bat' command for simulating deployment
                bat 'echo "Simulating file transfer to the staging server..." > deployment_log.txt'
                echo "Deployment simulation finished."
            }
        }
    }
    
    // Post-build actions: run at the end regardless of the stage result.
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

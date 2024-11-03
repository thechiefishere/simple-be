pipeline {
    agent any
    
    stages {
        stage("Checkout BE Repo") {
            steps {
                // Start an SSH session with your server
                sshagent(['3.81.15.121']) {
                    sh '''
                    ssh -o StrictHostKeyChecking=no ec2-user@3.81.15.121 '
                        # Navigate to the deployment directory
                        mkdir app
                        cd app &&
                        
                        # Pull latest code or files, if applicable
                        git clone https://github.com/thechiefishere/simple-be.git &&
                        
                        # Install dependencies, restart services, etc.
                        npm install &&
                        pm2 start server.js
                    '
                    '''
                }
            }
        }
    }
}

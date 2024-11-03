pipeline {
    agent any
    
    stages {
        stage("Checkout BE Repo") {
            steps {
                git credentialsId: '408c9adc-02e5-416e-89f5-61d6bb84d44c',
                url: 'https://github.com/thechiefishere/simple-be.git',
                branch: 'main'

                sh '''echo hello
                pwd
                ls'''

                git credentialsId: '408c9adc-02e5-416e-89f5-61d6bb84d44c',
                url: 'https://github.com/thechiefishere/simple-fe.git',
                branch: 'main'

                sh '''echo hello
                pwd
                ls'''
            }
        }
    }
}

pipeline {
    agent any
    
    stages {
        stage("Checkout Repo") {
            credentialsId: '408c9adc-02e5-416e-89f5-61d6bb84d44c',
            url: 'https://github.com/thechiefishere/simple-be.git',
            git branch: 'main'

            sh '''echo hello
            pwd
            ls'''
        }
    }
}

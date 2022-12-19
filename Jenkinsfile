pipeline {
    agent { label 'node3'}
    triggers {
        pollSCM('* * * * *')
    }
    stages{
        stage('vcs') {
            steps{
                git url: 'https://github.com/peddiraju3122b/saleor-dashboard.git',
                branch: 'main'
            }
        }
        stage('build image') {
            steps{
                sh 'docker image build -t peddiraju3122b/saleor-dashboard:DEV .'
            }
        }
        stage('push image to registry') {
            steps{
                sh 'docker image push peddiraju3122b/saleor-dashboard:DEV'
            }
        }
        
    }
}
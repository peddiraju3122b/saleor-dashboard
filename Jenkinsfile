pipeline{
    agent{ label 'node3'}
    trigger{
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
        
    }
}
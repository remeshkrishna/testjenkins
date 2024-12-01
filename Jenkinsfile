pipeline{
    agent any
    stages{
        stage('Fetch code from git'){
            steps{
                git branch: 'main', changelog: false, poll: false, url: 'https://github.com/remeshkrishna/testjenkins.git'
            }
        }
        stage('install apache'){
            steps{
                sh 'sudo apt install -y apache2'
            }
        }
        stage('Deploy app'){
            steps{
                sh 'sudo cp -R * /var/www/html/'
            }
        }
    }
}

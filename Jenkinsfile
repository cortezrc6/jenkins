pipeline {
    agent any

    stages {
        stage('Clone Repo') {
            steps {
                echo '[INFO] Cloning Repository'
             sh 'ls mywebsite'
             cleanWs()
            }
        }
        stage('Provision AWS Instance') {
            steps {
                echo '[INFO] Deploying to AWS'
            // sh 'scp -r mywebsite ec2-user@52.37.229.58:/var/www/html'
            }
        }
        stage('Deploy') {
            steps {
                echo '[INFO] Sending Notifications'
                // sh 'sh notif.sh'
            }
        }
        stage('Notification') {
            steps {
                echo '[INFO] Sending Notifications'
               // slackSend channel: '#random', message: 'test', teamDomain: 'randomresearchinc.slack.com', tokenCredentialId: 'slack'
              cleanWs()
            }
        }
    }
}
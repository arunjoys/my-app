  node{
   stage('SCM Checkout'){
     git 'https://github.com/arunjoys/my-app.git'
   }
   stage('Compile-Package'){
     sh label: '', script: 'mvn clean package' 
   }
   stage('Slack Notification'){
       slackSend baseUrl: 'https://hooks.slack.com/services/',
       channel: '#jenkins-pipeline-demo',
       color: 'good', 
       message: 'Welcome to Jenkins, Slack!', 
       teamDomain: 'javahomecloud',
       tokenCredentialId: 'slack-demo'
   }
}



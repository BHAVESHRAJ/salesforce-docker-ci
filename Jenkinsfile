pipeline {
    agent { docker { 
      args '--user=root'
      image 'curlybracket/salesforce:latest'
      } 
    }
    stages {
      stage ('Jenkins Start Notification') {
        steps {
          echo 'sending notification'
      }
    }
    }    
}

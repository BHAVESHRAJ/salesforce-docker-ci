pipeline {
    agent { docker { 
      args '--user=root'
      image 'salesforce/salesforcedx:latest-full'
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

pipeline {
    agent { docker { 
      args '--user=root'
      image 'salesforce/salesforcedx'
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

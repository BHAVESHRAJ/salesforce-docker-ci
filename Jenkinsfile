pipeline {
    agent {
        docker {
            image 'curlybracket/salesforce:latest'
            args '--user=root'
        }
    }
    environment {
        CI_ENVIRONMENT = credentials('CI_ENVIRONMENT')
        CI_ENVIRONMENT_URL = 'https://test.salesforce.com'
    }
   
    }
}

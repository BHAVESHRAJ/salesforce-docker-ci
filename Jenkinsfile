pipeline {
    agent {
        docker {
            image 'curlybracket/salesforce:latest'
            args '--user=root'
    stages {

        stage("Build") {
            steps {
                echo "building..."
      }
    }
        stage("Test") {
            steps {
                echo "testing..."
      }
    }
         stage("Package") {
            steps {
                echo "packaging..."
      }
    }
   
  }
 
}

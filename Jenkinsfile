pipeline {
    agent {
        docker {
        args '--user=root'
            image 'curlybracket/salesforce:latest'
        }
    }
    environment {
        CI_ENVIRONMENT = credentials('CI_ENVIRONMENT')
        CI_ENVIRONMENT_URL = 'https://test.salesforce.com'
    }
    stages {
        stage('Test') {
            steps {
                sh 'ant -buildfile /build/build.xml checkAndTest -Dbasedir=${WORKSPACE} -Dsfdc.username=${CI_ENVIRONMENT_USR} -Dsfdc.password=${CI_ENVIRONMENT_PSW} -Dsfdc.serverurl=${CI_ENVIRONMENT_URL}'
            }
            post {
                always {
                    junit 'testreports/*.xml'
                }
            }
        }
        stage('Deploy') {
            steps {
                sh 'ant -buildfile build/build.xml deployCode -Dsfdc.username=${CI_ENVIRONMENT_USR} -Dsfdc.password=${CI_ENVIRONMENT_PSW} -Dsfdc.serverurl=${CI_ENVIRONMENT_URL}'
            }
        }
    }
}

pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh './gradlew build'
            }
        }
        stage('docker') {
            steps {
                sh 'docker build . -t bowenjnr/phee:connector-mpesa'
                sh 'docker push bowenjnr/phee:connector-mpesa'
            }
        }
    }
}

pipeline {
    agent { docker 'maven:3.3.3' }
    stages {
        stage('build') {
            steps {
                sh '''
                   cd dt-ejb
                   mvn clean verify
                   cd ../Rest
                   mvn clean verify
                   cd ../web
                   mvn clean verify
                   cd ../daytrader-eeb
                   mvn clean verify
             }
        }
    }
}

pipeline {
    agent { label 'slave4' }
    stages {
        stage('checkout') {
            steps {
                sh 'rm -rf Parcel-service'
                sh 'git clone https://github.com/Chaitraradha/Parcel-service.git'
            }
        }
       stage('build') {
            steps {
                    sh 'mvn --version'
                    sh 'mvn clean install'
                  }
       }
    }
}

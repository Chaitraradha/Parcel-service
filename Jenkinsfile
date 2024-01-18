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
        stage('deploy') {
            steps {
                    sh 'scp /home/slave4/workspace/Pacel-services_feature-1/target/simple-parcel-service-app-1.0-SNAPSHOT.jar root@172.31.8.32:/opt/apache-tomcat-8.5.98/webapps'
                 }
           }
    }
}}   

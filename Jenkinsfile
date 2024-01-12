pipeline {
    agent any

    stages {
        stage('CLONE') {
            steps {
                git branch: 'main', url: 'https://github.com/Sharath-9632904366/my-app.git'
            }
        } 
        stage('CLEAN') {
            steps {
                sh  " mvn clean"
            }
        } 
        stage('TEST') {
            steps {
                sh  " mvn test"
            }
        } 
        stage('BUILD') {
            steps {
                sh  " mvn package"
            }
        } 
        stage('DEPLOY') {
            steps {
                sh  "scp target/app.war root@172.17.0.4:/opt/apache-tomcat-9.0.83/webapps"
            }
        }  
        stage('DOCKER_BUILD') {
            steps {
                sh  "docker build -t sharath4219/app:${BUILD_NUMBER}"
            }
        }  
    }
}

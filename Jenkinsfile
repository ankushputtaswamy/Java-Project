pipeline {
    agent any
    tools {
        jdk 'jdk11'
        maven 'maven3'
    }
    stages {
        stage('git checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/ankushputtaswamy/Java-Project.git'
            }
        }
        stage('mvn compile') {
            steps {
                sh "mvn clean compile"
            }
        }
        stage('mvn build') {
            steps {
                sh "mvn clean install"
            }   
        }
        stage('docker build & push') {
            steps {
                script {
                    withDockerRegistry(credentialsId: '89c6d379-af23-4049-97f7-88a1c145d5c9', toolName: 'docker') {
                        sh "docker build -t app:latest ."
                    }
                }
            }   
        }
    }
}

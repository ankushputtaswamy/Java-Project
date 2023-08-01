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
        stage('mvn build') {
            steps {
                sh "mvn clean install"
            }
        }
    }
}

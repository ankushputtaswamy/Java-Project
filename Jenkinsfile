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
    }
}

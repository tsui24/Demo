pipeline {
    agent any
    environment {
        JAVA_HOME = "/opt/java/jdk-21"
        PATH = "$JAVA_HOME/bin:$PATH"
    }
    tools {
        maven 'Maven_3.9.9'
    }
    stages {
        stage('Clone Source Code') {
            steps {
                git 'https://github.com/tsui24/Demo.git'
            }
        }
        stage('Build Project') {
            steps {
                sh 'mvn clean package'
            }
        }
        stage('Run Tests') {
            steps {
                sh 'mvn test'
            }
        }
    }
}
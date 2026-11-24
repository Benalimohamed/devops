pipeline {
    agent any

    tools {
        maven 'M2_HOME'
    }

    stages {
        stage('1 : Recuperation du code') {
            steps {
                git branch: 'back', 
                    url: 'https://github.com/Benalimohamed/devops.git'
            }
        }

        stage('2 : Build et Test') {
            steps {
                sh 'mvn clean test-compile compile'
            }
        }

        stage('3 : Package') {
            steps {
                sh 'mvn package -DskipTests'
            }
        }
    }
}//abc

#!/usr/bin/env groovy 

pipeline {
    agent any
    stages {

        stage('Build') {
            steps {
                if(isUnix() == true) {
                    sh "'mvn' -Dmaven.test.failure.ignore clean package"
                } else {
                    bat "'mvn' -Dmaven.test.failure.ignore clean package"
                }
            }
        }

        stage('Test') {
            steps {
                echo 'test'
            }
        }

        stage('Deployment') {
            steps {
                echo 'deploy'
            }
        }

    }
}

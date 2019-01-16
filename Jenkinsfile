#!/usr/bin/env groovy 

pipeline {
    agent any
    stages {

        stage('Build') {
            steps {
                sh "'mvn' -Dmaven.test.failure.ignore clean package"
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

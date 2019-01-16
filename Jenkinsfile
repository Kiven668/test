#!/usr/bin/env groovy 

pipeline {
    agent any
    stages {

        stage('Build') {
            steps {
                sh "'${MAVEN_HOME}/bin/mvn' -Dmaven.test.failure.ignore clean package"
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

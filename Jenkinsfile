#!/usr/bin/env groovy 

pipeline {
    agent any
    stages {

        stage('Build') {
            steps {
                script {
                    if(isUnix() == true) {
                        sh "'mvn' -Dmaven.test.failure.ignore clean package"
                    } else {
                        bat "mvn -Dmaven.test.failure.ignore clean package"
                    }
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
                script {
                    if(isUnix() == true) {
                        sh "cf push"
                    } else {
                        bat "cf push"
                    }
                }
            }
        }

    }
}

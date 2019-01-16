#!/usr/bin/env groovy 

pipeline {
    agent any
    options {
        timeout(time: 120, unit: 'MINUTES')
        timestamps()
        buildDiscarder(logRotator(numToKeepStr: '10', artifactNumToKeepStr: '10'))
        skipDefaultCheckout()
    }
    stages {

        stage('Build') {
            sh "'${MAVEN_HOME}/bin/mvn' -Dmaven.test.failure.ignore clean package"
        }

        stage('Test') {
            echo 'test'
        }

        stage('Deployment') {
            echo 'deploy'
        }

    }
}

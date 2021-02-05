#!/usr/bin/env groovy
pipeline {
    agent any
    options {
        ansiColor('xterm')
    }
    stages {
        stage('Test') {
            steps {
                withGradle {
                    sh './gradlew test'
                }
            }
            post {
                always {
                    junit 'build/test-results/**/TEST-*.xml'
               }
            }
        }
    }
}

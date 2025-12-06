pipeline {
        agent any
        tools {
                nodejs 'node-20'
        }
        stages {
                stage ('Clone') {
                        steps {
                                echo 'Cloning repository...'
                        }
                }
                stage ('Install Dpendencies'){
                        steps {
                                sh 'npm install'
                        }
                }
                stage ('Run Tests') {
                        steps {
                                sh 'npm test'
                        }
                }
                stage ('Build') {
                        steps {
                                sh 'docker build -t mohamed2003/node-ci:1.0 .'
                        }
                }
        }
}
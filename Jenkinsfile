pipeline {
        agent any
        tools {
                node 'node-20'
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
                                echo 'Build stage completed (demo)'
                        }
                }
        }
}
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
                                echo 'ggg'
                                echo 'Build stage completed (demo)'
                        }
                }
        }
}
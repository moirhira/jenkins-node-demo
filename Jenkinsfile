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
                stage ('Docker Build') {
                        steps {
                                sh 'docker build -t mohamed2003/node-ci:1.0 .'
                        }
                }
                stage ('Docker push') {
                        steps {
                                withCredentials([usernamePassword(credentialsId: '21552dec-fd1a-48cc-b53e-6d55fa3df9a2	', usernameVariable: 'USER', passwordVariable: 'PASS')]) {

                                        {
                                                sh 'echo $PASS| docker login -u $USER --password-stdin'
                                                sh 'docker push mohamed2003/node-ci:1.0'
                                        }
                        }
                }
        }
}
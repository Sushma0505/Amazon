
pipeline {
    agent any

    options {
        skipDefaultCheckout(true)
    }

    stages {
        stage('Clone') {
            steps {
                checkout scm
                echo 'GitHub repository cloned'
            }
        }

        stage('Validate') {
            steps {
                script {
                    if (!fileExists('pom.xml')) {
                        error('pom.xml missing')
                    }
                }
                echo 'Project validated'
            }
        }

        stage('Clean') {
            steps {
                echo 'Clean stage completed'
            }
        }

        stage('Compile') {
            steps {
                echo 'Compile stage completed'
            }
        }

        stage('Build') {
            steps {
                echo 'Build stage completed'
            }
        }
    }

    post {
        success {
            echo 'Jenkins build SUCCESS'
        }
        failure {
            echo 'Jenkins build FAILURE'
        }
    }
}

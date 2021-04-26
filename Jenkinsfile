pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                dockerfile {
                    filename 'Dockerfile'
                    dir '.'
                    label 'latest'
                }
            }
        }
        stage('Test') {
            steps {
                docker {
				image 'ps3dev-docker'
				label 'latest'
				}
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}

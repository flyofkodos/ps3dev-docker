pipeline {
	agent {label 'Centosdocker'}

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
            agent {
                docker {
				image 'ps3dev-docker'
				label 'latest'
				}
            }
            steps {
                sh 'hostname'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}

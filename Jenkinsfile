pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                app = docker.build(ps3dev-docker)
            }
        }
        stage('Test') {
            steps {
                app.inside {echo 'Testing..'}
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}

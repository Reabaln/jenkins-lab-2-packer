pipeline {
    agent { docker { image 'bryandollery/alpine-docker' } }
    stages {
        stage('build') {
            environment {
               CREDS = credentials('reab-creds')
            }
            steps {
                sh "make"
		sh "make build"
            }
        }
    }
}

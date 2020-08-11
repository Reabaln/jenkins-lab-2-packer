pipeline {
    agent { docker { image 'bryandollery/aws-cli-alpine' } }
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

pipeline {
    agent { docker { image 'bryandollery/terraform-packer-aws-alpine' } }
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

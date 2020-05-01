
pipeline {
    agent any
    stages {
        stage('Upload to AWS') {
            steps {
                sh 'echo "Hello World"'
                withAWS(region:'us-east-2') {
                    withAWS(credentials:'aws-static') {
                s3Upload(file:'index.html', bucket:'udacity-pipeline', path:'index.html')
                }
                }                
            }
        }
    }
}

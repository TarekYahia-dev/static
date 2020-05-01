
pipeline {
    agent any
    stages {
        stage('Upload to AWS') {
            steps {
                sh 'echo "Hello World"'
                withAWS(region:'us-east-2') {
                    withAWS(credentials:'jenkins') {
                s3Upload(file:'index.html', bucket:'my-bucket', path:'index.html')
                }
                }                
            }
        }
    }
}

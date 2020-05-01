
pipeline {
    agent any
    stages {
        stage('Upload to AWS') {
            steps {
                sh 'echo "Hello World"'
                withAWS(region:'us-east-2') {
                    withAWS(credentials:'AWS Access Key: AKIAQ2Z4X347FQ55FDVP, AWS Secret Key: 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') {
                s3Upload(file:'index.html', bucket:'my-bucket', path:'index.html')
                }
                }                
            }
        }
    }
}

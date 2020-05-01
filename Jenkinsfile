pipeline {
    agent any
    stages {
	    stage('Lint HTML'){
           steps{
             echo 'hello world'   
             sh 'tidy -q -e *.html'
			}
		} 
        stage('Upload to AWS') {
            steps {
                sh 'echo "Hello World"'
                withAWS(region:'us-east-2') {
                    withAWS(credentials:'aws-static') {
                s3Upload(file:'index.html', bucket:'udacity-pipeline', path:'index.html')
                }}                
            }
		}
        
	}
}

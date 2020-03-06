pipeline {
    agent any
    stages {
       stage('Build') {
             steps {
                 sh 'tidy -q -e *.html'
             }
       }
        stage('Upload to AWS.') {
           steps {
                 sh 'echo "Hello World"'
                 sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                 '''
               withAWS(credentials: 'jenkins', region: 'ap-northeast-1a')  {
                s3Upload(bucket: 'jenkinsdevops12', file: 'index.html')
               
               
               }
                 }
             }
        
        }
    }

pipeline {
    agent any
    stages {
       stage('Upload to AWS') {
             steps {
                 withAWS(credentials: 'aws-static', region: 'ap-northeast-1a')  
                 sh ' "Hello" '
                    s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'index.html', bucket:'jenkinsdevops12')
              
                 
              
                 }
             }
        }
    }

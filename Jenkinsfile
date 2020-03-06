pipeline {
    agent any
    stages {
       stage('Upload to AWS') {
             steps {
                 withAWS(endpointUrl:'http://jenkinsdevops12.s3-website-ap-northeast-1.amazonaws.com',credentials: 'aws-static', region: 'ap-northeast-1a')  
                 s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'index.html', bucket:'jenkinsdevops12')
              
              
                 }
             }
        }
    }

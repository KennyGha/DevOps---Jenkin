pipeline {
    agent any
    stages {
       stage('Lint HTML') {
             steps{
                
                script '{tidy -q -e /home/ubuntu/devops/static/index.html}'
           }   
       
       }
       stage('Upload to AWS') {    
             steps {
                 withAWS(region:'ap-northeast-1',credentials:'aws-static') {
                 sh 'echo "Uploading content with AWS creds"'
                     s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'index.html', bucket:'jenkinsdevops12')
                 }
             }
        }
        
    }
}

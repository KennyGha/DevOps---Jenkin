pipeline {
    agent any
    stages {
       stage('Lint HTML') {
             steps{
                
                script {tidy -q -e index.html}
           }   
       
       }
       stage('Lint HTML') {    
             steps {
                 withAWS(region:'ap-northeast-1',credentials:'aws-static') {
                 sh 'echo "Uploading content with AWS creds"'
                     s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'index.html', bucket:'jenkinsdevops12')
                 }
             }
        }
    }
}

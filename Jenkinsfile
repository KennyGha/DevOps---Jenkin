pipeline {
    agent any
    stages {
       stage('Build') {
             steps {
                 withAWS(endpointUrl:'http://jenkinsdevops12.s3-website-ap-northeast-1.amazonaws.com',credentials: 'AKIAV4WC4AJ325YEFNC7', region: 'ap-northeast-1a')  
                 sh 'echo "Hello World"'
                 sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                 '''
                 }
             }
        }
    }

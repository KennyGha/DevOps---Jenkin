pipeline {
    agent any
    stages {
       stage('Lint HTML') {
             steps {
                 script {tidy -q -e index.html}}
             }
        }
    }
}

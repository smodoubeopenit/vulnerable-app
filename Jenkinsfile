pipeline {
    agent any
    tools {
        nodejs 'NodeJS-15.10.0'
    }
  
    stages {
        stage('Build') {
            steps {
                
                sh 'npm build'
            }
        }
    stage('Code Analysis') {
            steps {
                sh '/usr/local/bin/sl analyze --app AngularShiftLeft --js --cpg ./...'
               
            }
       }
    }
}

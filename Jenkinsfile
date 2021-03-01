pipeline {
    agent any
    tools {
        go 'go-1.16'
    }
  
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
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

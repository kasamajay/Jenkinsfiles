```
pipeline {
    agent none

    stages {
        stage('nodejs') {
            agent {
              docker { image 'node:16-alpine' }
            }
            steps {

                sh 'node --version'
            }
        }
        
        stage('maven') {
            agent {
              docker { image 'maven:3.8.1-adoptopenjdk-11' }
            }
            steps {
                sh 'mvn --version'
            }
        }
        
    }
}
```

```
pipeline {
    agent {
      docker { image 'node:16-alpine' }
    }

    stages {
        stage('Hello') {
            steps {
                sh 'env'
                sh 'echo $USER'
                sh 'node --version'
            }
        }
    }
}
```

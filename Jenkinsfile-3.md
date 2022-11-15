```pipeline {
    agent { dockerfile true }

    stages {
        stage('dockerfile-agent') {
            steps {
                sh '''
                    node --version
                    git --version
                    curl --version
                '''
            }
        }
    }
}
```

pipeline {
    agent any
    stages {
        stage('Verify Branch') {
            steps {
                echo "$GIT_BRANCH"
            }
        }
        stage('Build') {
            steps {
                sh '''docker images -a
                cd azure-vote/
                docker build -t azure-vote .
                docker images -a
                cd ..'''
            }
        }
        
    }
}

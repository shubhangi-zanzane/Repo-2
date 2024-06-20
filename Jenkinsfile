pipeline {
    agent any
    triggers {
        githubPush()
    }
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/shubhangi-zanzane/Repo-2.git'
            }
        }
        stage('Build') {
            steps {
                sh 'echo "hello"'
            }
        }
    }
}

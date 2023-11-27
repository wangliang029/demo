pipeline {
    agent any
    stages {
        stage ('Build'){
            steps{
                echo "get code from github"
                git branch: 'master', url: 'https://github.com/wangliang029/demo.git'
            }
        }
    }
}

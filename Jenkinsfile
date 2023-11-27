pipeline {
    agent any
    stages {
        stage ('pull code'){
            steps{
                echo "get code from github"
                git branch: 'master', url: 'https://github.com/wangliang029/demo.git'
            }
        }
        stage ('Build'){
            steps{
              echo "build project"
              sh '''
                 mvn clean
                 mvn clean install -DskipTests '''
            }
        }
    }
}

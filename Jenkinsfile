pipeline {
    agent any
    stages {
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

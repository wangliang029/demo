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
              echo $JAVA_HOME
              echo $MAVEN_HOME
              sh '''
                 export JAVA_HOME=/Library/Java/JavaVirtualMachines/jdk1.8.0_311.jdk/Contents/Home
                 export MAVEN_HOME=/opt/homebrew/Cellar/maven/3.9.5
                 echo $JAVA_HOME
                 echo $MAVEN_HOME
                 mvn clean
                 mvn clean install -DskipTests '''
            }
        }
    }
}

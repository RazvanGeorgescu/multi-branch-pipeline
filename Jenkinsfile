pipeline {
    environment {
        JAVA_TOOL_OPTIONS = "-Duser.home=/home/jenkins"
    }
    agent {
        dockerfile {
            image "maven:3.6.0-jdk-13"
            label "master"
            args "-v /tmp/maven:/home/jenkins/.m2 -e MAVEN_CONFIG=/home/jenkins/.m2"
        }
    }
    
    stages {
      stage("build") {
        steps {
            sh "ssh -v"
            sh "mvn -version"
        }
      }
    }
}

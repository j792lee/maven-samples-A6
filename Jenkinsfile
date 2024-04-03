pipeline {
  agent any
  stages {
    stage('check out') {
      steps {
        git 'https://github.com/j792lee/maven-samples-A6'
      }
    }

    stage('run') {
      steps {
        powershell 'git bisect start 198644632661c67b6c32f59e9047c11a70685e15 98ac319c0cff47b4d39a1a7b61b4e195cfa231e5'
        powershell 'git bisect run mvn clean test'
      }
    }

  }
  tools {
    maven 'DHT_MAVEN'
    jdk 'DHT_SENSE'
  }
}
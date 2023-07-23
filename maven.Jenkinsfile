pipeline {
    agent any
  stages {
       stage('initial') {
      steps {
       
       bat "git clone  https://github.com/kasiteja007/simple-java-maven-app.git"
       bat "mvn clean -f simple-java-maven-app"
          
       }
    }
    
    stage('Build') {
      parallel {
        stage ('First Test') {
          steps {
            echo 'Run First Test here...'
          }
        }
        stage('Second Test') {
          
            steps {
                bat "mvn -B -DskipTests clean package -f simple-java-maven-app"
            }
          }
        }
      }
    }
  }

pipeline {
    agent any

    stages {
        stage('Hello') {
          steps {
            echo 'Hello, World!'
          }
        }
        
        stage('Test Maven') {
          steps {
            sh """mvn -version"""
          }
        }
        
        stage('Checkout Git') {
            steps {
                echo 'Pulling from git ...';
                git branch: 'main',
                    url: "https://github.com/khalilDimassi/oswin-devops-project";
            }
        }

        stage('MVN CLEAN') {
          steps {
            sh 'mvn clean'
          }
        }

        stage('MVN COMPILE') {
          steps {
            sh 'mvn compile'
          }
        }

    //   stage('Build') {
    //       steps {
    //           // Your build steps here
    //       }
    //   }

    //   stage('Test') {
    //       steps {
    //           // Your test steps here
    //       }
    //   }

    //   stage('SonarQube analysis') {
    //       steps {
    //           withSonarQubeEnv('SonarQube') {
    //               // Your SonarQube analysis steps here
    //               sh "${env.SONAR_SCANNER_HOME}/bin/sonar-scanner"
    //           }
    //       }
    //   }
    }
}

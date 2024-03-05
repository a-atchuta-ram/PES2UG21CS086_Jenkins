  pipeline {
    agent any
    stages {
      stage('Build') {
            steps {
               build 'PES2UG21CS086-1'
                sh 'g++ t1.cpp -o output' 
                //sh 'aaag++ t1.cpp -o output'
               catchError {
                    sh './gradlew compileJava --stacktrace'
                }
            }
        }
      stage('Test') {
            steps {
               sh './output'
            }
        }
      stage('Deploy') {
         steps {
               echo 'deploy'
            }
      }
    }
      post{
         failure{
               echo 'Pipeline Failed'
    }
  }
}

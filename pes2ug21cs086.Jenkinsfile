  pipeline {
    agent any
    stages {
      stage('Build') {
            steps {
               111build 'PES2UG21CS086-1'
               sh 'g++ t1.cpp -o output'
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

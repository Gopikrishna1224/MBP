pipeline {
   agent any
   stages {
       stage('Build Code') {
           steps {
               sh """
               echo "Building Artifact"
               """
           }
       }
      stage ('reading branch wise')
      {
      when
      {
      branch "feature*"
      }
      steps
      {
      echo " It is only for feature branch "
      }
      }
      stage('Deploy Code') {
          steps {
               sh """
               echo "Deploying Code"
               """
          }
      }
   }
}

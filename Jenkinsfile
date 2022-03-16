pipeline {
   agent any
   stages {
       stage('Build Code') {
           steps {
               sh "mvn clean package"
	       echo building artifact for project samplewebapp"

               
               }
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
          when {
	         branch "master"
		 }
               steps
	       {
	       sh "mvn tomcat7:deploy"
	       echo "deploying code"
	       }
              
          }
      }
   


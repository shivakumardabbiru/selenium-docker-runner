pipeline{
	agent any
	stages{
	  stage("run test"){
	     steps{
	          bat "docker-compose up"
	     }
	  }
      stage("Bring hub down"){
         steps{
              bat "docker-compose down"
         }
      }
	}
}
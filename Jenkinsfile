pipeline{
	agent any
	stages{
	  stage("start hub"){
	     steps{
	          bat "docker-compose up -d hub chrome firefox"
	     }
	  }
	  stage("Run Test"){
	  	steps{
	  		bat "docker-compose up searchtesting1 bookflight1"
	  	}
	  }
      stage("Bring hub down"){
         steps{
              bat "docker-compose down"
         }
      }
	}
}
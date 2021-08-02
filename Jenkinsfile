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
	}
    post{
     always{
     	 	archiveArtifacts artifacts: 'output/**'
     	 	bat "docker-compose down"
     	 }
     }
}
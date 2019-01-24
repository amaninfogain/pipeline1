pipeline {
    agent any
	
	parameters {
        string(name: 'id', defaultValue: 'aman', description: 'Enter your name')
    }
  
     

libraries {
  lib('myvar@master')
}
     

    stages{
      stage('demo') {
          steps {
		  script{	  
                    hello.call "${params.id}"
	            sh 'lscpu'	  
		  }
           }
        }
	    
      stage('deploy') {
	      environment {
        source =  '/home/xavient/git/pipeline/data'
        target =  '/home/xavient/git/pipeline/data2'
      }
          steps {
		  script{	  
                    
			  copy.call ("${env.source}","${env.target}")
		  }
		  
	  }
      }
      }
}

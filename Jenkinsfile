pipeline {
    agent any
	
	parameters {
        string(name: 'id', defaultValue: 'aman', description: 'Enter your name')
    }
  
     

libraries {
  lib('myvar@master')
}
     environment {
        source = /home/xavient/git/pipeline/data
        target = /home/xavient/git/pipeline/data2
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
          steps {
		  script{	  
                    
	            copy.call 'aman'		  
		  }
           }
        }
      
      
      }
}

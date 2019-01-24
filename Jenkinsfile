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
		    sh 'pwd'
	            sh 'cp -rf /tmp/data /tmp/data2'	  
		  }
           }
        }
	    
      stage('deploy') {
	      environment {
        source =  '/home/xavient/git/pipeline/data'
        target =  '/home/xavient/git/pipeline/data2'
      }
          steps {
		  
		  echo "${env.source}"
		  script{	  
                         
			  run.call ("${env.source}","${env.target}")
		  }
		  
	  }
      }
      }
}

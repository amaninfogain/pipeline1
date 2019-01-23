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
	            hello.now "/home/xavient/india,/home/xavient/git"		  
		  }
           }
        }
      
      
      }
}

pipeline {
    agent any
	
	parameters {
        string(name: 'id', defaultValue: 'aman', description: 'Enter your name')
    }

     environment {
        
        source = /home/xavient/git/pipeline/data
        target = /home/xavient/git/pipeline/data2
      }

libraries {
  lib('myvar@master')
}

    stages{
      stage('demo') {
          steps {
             hello "${params.id}"
           }
        }
      stage('Deploy') {
          steps {
             copy "${source},${target}"
           }
        }
      
      }
}

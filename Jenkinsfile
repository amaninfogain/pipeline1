pipeline {
    agent any
   
        environment { 
        source = /home/xavient/git/pipeline/data
        target = /home/xavient/git/pipeline/data2
      }
	
	parameters {
        string(name: 'id', defaultValue: 'aman', description: 'Enter your name')
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
             copy "${env.source},${env.target}"

           }
        }
      }
}

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
             hello "${params.id}"
           }
        }
      stage('Deploy') {
          steps {
             sh 'lscpu'
           }
        }
      }
}

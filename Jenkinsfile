pipeline {
    agent any
	
	parameters {
        string(name: 'userFlag', defaultValue: 'aman', description: 'Enter your name')
    }

libraries {
  lib('myvar@master')
}

    stages{
      stage('demo') {
          steps {
             hello '${env.name}'
           }
        }
      }
}

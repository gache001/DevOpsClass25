pipeline {
    agent {
        node {
            label 'slave'
        }
    }
    parameters {
    	string(name: 'serverIP', defaultValue: '10.10.10.25', description: 'Enter Server IP.. ')
	string(name: 'servername', defaultValue: 'None', description: 'Enter Ansible slave name ')
	password(name: 'dockerpass', description: 'Enter docker login password ')	    
    }
    stages {
	    stage('checkout'){
		    steps{
		    checkout scm
		    }
	    }
	stage('Remove dockers'){
	    steps {
		//sh "if [ `sudo docker ps -a -q|wc -l` -gt 0 ]; then sudo docker rm -f \$(sudo docker ps -a -q);fi"
		    sh "echo Remove dockers"
		}
	}
	stage('Build'){
	    steps {
		    sh "cd ${WORKSPACE}"
		    //sh "sudo docker build -t devopsdemo ."
		    sh "echo Build"
	   }
	}
	   
}

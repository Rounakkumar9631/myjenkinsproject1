pipeline {

agent any 

stages {
	stage ('Code Checkout') {
		steps { 
			git 'https://github.com/Rounakkumar9631/myjenkinsproject1.git'
			}
		}
	stage ('Build Docker image') {
		steps {
			sh 'docker build -t myapp:latest .'
			}
		}
	stage ('Run Test') {
		steps {
			sh 'echo Running tests...'
			}
		}
	stage ('push Docker image') {
		steps {
			sh '''
			docker tag myapp:latest rounakj06/myapp:latest
			docker push rounakj06/myapp:latest
			'''
			}
		}
	stage ('Deploy to Kubernetes') {
		steps {
			sh 'kubectl apply -f deployment1.yaml'
			}	
		}
	}
}

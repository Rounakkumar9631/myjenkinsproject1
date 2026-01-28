pipeline {

agent any 

stages {
	stage ('SCM') {
		steps { 
			echo "git pull my code"
			}
		}
	stage ('Deploy') {
		steps {
			echo "deploy my code"
			}
		}
	stage ('Test') {
		steps {
			echo "test my code"
			}
		}
	}
}
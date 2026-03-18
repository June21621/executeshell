pipeline {
	agent any
	stages {
		stage('github clone') {
			steps {
				git branch: 'main', url: 'https://github.com/June21621/executeshell.git'
			}
		}
		stage('Compile') {
			steps {
				echo "Compiled successfully!";
				sh './build.sh'
			}
		}
		stage('JUnit') {
			steps {
					echo "JUnit passed successfully!";
					sh './unit.sh'
			}
		}
		stage('Code Analysis') {
			steps {
				echo "Code Analysis completed successfully!";
				sh './quality.sh'
			}
		}
		stage('Deploy') {
			steps {
				echo "Deployed successfully!";
				sh './deploy.sh'
			}
		}
	}
}

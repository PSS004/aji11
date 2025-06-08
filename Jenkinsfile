pipeline{
	agent any
	tools{
		maven 'maven'
	}
	stages{
		stage('checkout'){
			steps{
				git branch:'master', url:'https://github.com/PSS004/aji11.git'
			}
		}
		stage('Build'){
			steps{
				sh 'mvn clean install'
				}
			}
		stage('Test')
		{
			steps{
				sh 'mvn test'
			}
		}
		stage('run applications')
		{
			steps{
				sh 'java -jar target/maven99-1.0-SNAPSHOT.jar'
			}
		}
	}
	post{
		success{
			echo 'success'
			}
		failure{
			echo 'failure'
			}
		}
	}

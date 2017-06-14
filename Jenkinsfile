node {
	   stage('Preparation') { // for display purposes
	      // Get some code from a GitHub repository
	      git credentialsId: '296cec77-12a9-4979-ae2b-3616c6e0b363', url: 'git@github.com:Soya93/romannumerals.git'
	      // Get the Maven tool.
	      // ** NOTE: This 'M3' Maven tool must be configured
	      // **       in the global configuration.           
	      
	   }
	   stage('Build') {
	      // Run the maven build
	      if (isUnix()) {
	         sh "mvn -Dmaven.test.failure.ignore clean package"
	      }
	   }
	   stage('Results') {
	      junit '**/target/surefire-reports/TEST-*.xml'
	      archive 'target/*.jar'
	   }
	}

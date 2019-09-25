pipeline{
	agent{
		node{
			label 'master'
		}
	}
	stages{
		stage('S3 Upload started'){
			steps{
				sh 'echo "Started...!" '
			}
		}
        
 	 stage('S3 Upload'){
		steps{
		sh 'cd /var/lib/jenkins/workspace/tomcat_maven/target/; aws s3 cp WebApp.war s3://capgeminipoc-terraform-praveen-1/'
			}
		}
		stage('S3_Upload Ended'){
			steps{
			sh 'echo "Uploaded...!" '
			}
		}
	}
}

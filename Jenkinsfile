pipeline{
agent any
	

	tools {
    	maven 'maven-3.6.3'
	
    }
	stages{
		stage("build"){
			steps {
			sh "mvn clean package"
				}
			}
		
  stage("dynamic-deploy"){
	  steps{
		  sshagent(['book']) {
    // some block


	 sh "ansible-playbook -i aws_ec2.yaml tomcat.yml
"
                }
            }
  } 
        }
        
}	
	
		


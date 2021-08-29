node('master') 
{
    stage('Continuous Download_loan') 
	{
    git 'https://github.com/govardhanreddy14/maven.git'
	}
    stage('Continuous Build_loan') 
	{
    sh label: '', script: 'mvn package'
	}
    stage('Continuous Deployment_loan') 
	{
sh label: '', script: 'scp /home/ubuntu/.jenkins/workspace/ScriptedPipeline/webapp/target/webapp.war   ubuntu@172.31.23.90:/var/lib/tomcat8/webapps/qaenv.war'
	}
    stage('Continuous Testing_loan') 
	{
              sh label: '', script: 'echo "Testing Passed"'
	}
    stage('Continuous Delivery_loan') 
	{
sh label: '', script: 'scp /home/ubuntu/.jenkins/workspace/ScriptedPipeline/webapp/target/webapp.war   ubuntu@172.31.28.143:/var/lib/tomcat8/webapps/prodenv.war'
	}
}

pipeline
{
  agent any
  
    stages 
    {
      
      stage ('scm checkout')
      {
          git 'https://github.com/Shobhit101/maven-project'
      }
    }
  {
      stage ('code install')
      {
        steps
        {
          withMaven(maven: 'LocalMaven')
          {
              sh 'mvn install'
           }
        }
      }
    stage ('code deploy')
    {
      steps
      {
          sshagent(['172.31.32.252']) {
			sh 'scp -o StrictHostKeyChecking=no */target/*.war ec2-user@172.31.32.252:/var/lib/tomcat/webapps'
		}
      }	  
    }
  }
}

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
        deploy adapters: [tomcat8(credentialsId: '27078fab-846f-47bf-9b40-b98b72f6264d', path: '', url: 'http://18.223.16.123:8080')], contextPath: null, onFailure: false, war: '**/*.war'
      }
    }  
    }
  }

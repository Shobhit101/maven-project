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
    }
  }

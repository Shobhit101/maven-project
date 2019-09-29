pipeline
{
  agent any
  
    stages 
    {
      {
      stage ('scm checkout')
        steps
        {
      {
          git 'https://github.com/Shobhit101/maven-project'
      }
        }
      stage ('code test')
      {
        steps
        {
          withMaven(maven: 'LocalMaven')
          {
              sh 'mvn test'
           }
        }
      }
    }
  }

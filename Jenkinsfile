pipeline
{

  agent any
  {

stages {
stage ('scm checkout') {

git 'https://github.com/Shobhit101/maven-project.git'
}

stage ('code test') {
withMaven(maven: 'LocalMaven') {
    sh 'mvn test'
}
}
}
}
}

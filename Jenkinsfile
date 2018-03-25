node{
  stage ('Build') {

    git url: 'https://github.com/prasanthbangs2016/jenkins-example'

    withMaven(
        // Maven installation declared in the Jenkins "Global Tool Configuration"
        maven: 'M3',
        // Maven settings.xml file defined with the Jenkins Config File Provider Plugin
        // Maven settings and global settings can also be defined in Jenkins Global Tools Configuration
        
        mavenLocalRepo: '.repository') {

      // Run the maven build
      sh "mvn clean install"

    } // withMaven will discover the generated Maven artifacts, JUnit Surefire & FailSafe & FindBugs reports...
  }
}

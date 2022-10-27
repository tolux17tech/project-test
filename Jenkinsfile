// @Library('test-shared-library') _
// import com.example.*

// new Pipeline(this, "config.yml").execute()


node
  {
   def mavenHome = tool name: 'maven'
  stage('1.git clone')
  {
  git credentialsId: 'GitCredentials', url: 'https://github.com/tolux17tech/project-test.git'
  }
  stage('2.maven-Build')
  { 
    sh 'mvn --version'
  }
  stage('3.CodeQualityReport')
  {
     withSonarQubeEnv(credentialsId: 'sonarqubeconfigured') {
     sh 'mvn sonar:sonar'
    }
  }
 stage('4.UploadWarNexus')
        {
        //sh '${mavenHome}/bin/mvn clean deploy'
        }
 stage('5.DeployTomcat')
        {
          // blocks
       // deploy adapters: [tomcat9(credentialsId: 'Tomcat_Credentials', path: '', url: 'http://3.85.28.18:7777/')], contextPath: null, war: '**/*.war'
        }   
  } 
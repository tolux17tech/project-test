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
  stage('mvn version'){
    sh "${mavenHome}/bin/mvn clean package"
   }

  }





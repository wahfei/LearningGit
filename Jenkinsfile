pipeline{

  agent any
  
  stages {
    
    stage("build") {
      steps{
        echo "currently building application"
        // Checkout
        git branch: 'master',url: 'https://github.com/devops81/HTMLPublisher.git&#8217;

        // Checkout
        git branch: 'master',url: 'https://github.com/devops81/HTMLPublisher.git&#8217;

        // install required bundles
        sh 'bundle install'

        // build and run tests with coverage
        sh 'bundle exec rake build spec'

        // Archive the built artifacts
        archive (includes: 'pkg/*.gem')
        
        publishHTML([
          allowMissing: false, 
          alwaysLinkToLastBuild: false, 
          keepAll: false, 
          reportDir: 'coverage', 
          reportFiles: 'index.html', 
          reportName: 'HTML Report', 
          reportTitles: 'Coverage Report'])
      }
    }
     stage("test") {
      steps{
        echo "currently testing application"
      }
    }
    
     stage("deploy") {
      steps{
        echo "currently deploying application"      
      }
    }
    
  }
}

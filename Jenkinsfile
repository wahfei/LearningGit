pipeline{

  agent any
  
  stages {
    
    stage("build") {
      steps{
        echo "currently building application"
//         publishHTML (target : [
//           allowMissing: false,
//           alwaysLinkToLastBuild: true,
//           keepAll: true,
//           reportDir: '',
//           reportFiles: 'index.html',
//           reportName: 'My Reports',
//           reportTitles: 'The Report'])
        
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

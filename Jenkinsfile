node{
    stage('GIT checkout'){
           git 'https://github.com/BalajiKannappa/simple-app'
        }
    stage('Maven compile-package'){
            sh "mvn package"
        }
    stage('Sonarqube anlaysis'){
              withSonarQubeEnv('sonar-qube'){
                sh "mvn sonar:sonar"  
               }
        }
   
    stage("Quality Gate Status Check"){
          timeout(time: 1, unit: 'HOURS') {
              def qg = waitForQualityGate()
              if (qg.status != 'OK') {
                   echo "Status check failed"
              }
              else{
                  echo "Status check passed"
              }
          }
      }    
 


}

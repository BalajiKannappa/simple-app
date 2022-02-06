node{
    stage('GIT checkout'){
     
             git 'https://github.com/BalajiKannappa/simple-app'
        }
    
    stage('Maven compile-package'){
    
            sh "mvn package"
        }
    

    stage('Static code anlaysis'){
    
            withSonarQubeEnv('sonar-qube'){
                sh "mvn sonar:sonar"  
               }
        }

    


}

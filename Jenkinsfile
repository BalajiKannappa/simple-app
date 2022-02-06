node{
    stage('GIT checkout'){
        steps{
             git 'https://github.com/BalajiKannappa/simple-app'
        }
    }
    stage('Maven compile-package'){
        steps{
            sh "mvn package"
        }
    }

    stage('Static code anlaysis'){
        steps{
            WithSonarQubeEnv('sonar-qube'){
                sh "mvn sonar:sonar"            }
        }

    }



}

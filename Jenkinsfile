node{
    stage('GIT checkout'){
        git 'https://github.com/BalajiKannappa/simple-app'
    }
    stage('Maven compile-package'){
        sh "mvn package"
    }

}

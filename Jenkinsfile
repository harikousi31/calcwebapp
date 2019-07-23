node{
    stage('cloning git'){
        git 'https://github.com/harikousi31/calcwebapp.git'
    }
    stage('build'){
        def mvnHome = tool name: 'maven', type: 'maven'
        sh "${mvnHome}/bin/mvn package"
    }
    stage('Deploy to Tomcat'){ 
        sh 'cp target/*.war /opt/tomcat/webapps'
    }    
}

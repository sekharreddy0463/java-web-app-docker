pipeline{
    agent any
    stages{
        stage("checkout stage"){
            steps{
        git 'https://github.com/sekharreddy0463/java-web-app-docker.git'
    }
}
stage("build"){
    steps{
        sh "mvn clean install"
    }
}
stage("test"){
    steps{
        sh "mvn test"
    }
}
stage('deploy code'){
        steps{
        deploy adapters: [tomcat8(credentialsId: 'tomcat.crediantls', path: '', url: 'http://54.234.184.118:8090/')], contextPath: null, war: '**/*.war'
}
}
}
}

node{
    stage('SCM'){
        git 'https://github.com/nehasri17/maven-simple.git'    
    }
    stage('Package'){
        sh 'mvn clean package install deploy'
    }
    stage('artifacts'){
        archiveArtifacts 'target/*.jar'
    }
    stage('test results'){
        junit 'target/surefire-reports/*.xml'
    }
}
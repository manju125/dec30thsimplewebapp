pipeline {
    agent any

    stages{
        stage('CleaningStage'){
            steps{
                git "https://github.com/manju125/dec30thsimplewebapp.git"
                bat "mvn clean"
            }
        }
        stage('TestingStage'){
            steps{
                bat "mvn test"
            }
        }
        stage('PackaingStage'){
            steps{
                bat "mvn package"
            }
        }
        stage('DeployStage'){
            steps{
              bat "mvn tomcat7:undeploy tomcat7:deploy"
            }  
        }
        
        
    }
}

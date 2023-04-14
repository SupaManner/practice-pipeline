pipeline{
    agent any 
    tools {
        maven 'MAVEN'  
    }
    stages{
        stage("Cloning"){
            // Need to clone the repo into the workspace
            steps{
                git changelog: false, poll: false, url: 'url: 'https://github.com/SupaManner/practice-pipeline.git'
            } 
        }
        stage("Building"){
            // Need to build the code using maven
            steps{
                sh 'mvn -B -DskipTests clean package'
            }
        }
    }
}

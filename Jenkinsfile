pipeline{
    agent any
    tools {
        gradle "Gradle"
    }
    stages{
        stage("Cloning repository"){
            steps{
                git branch:"master", url:"https://github.com/MiriamNyaga/gallery.git"
            }
        }
        
        stage("Building code"){
            steps{
                sh "gradle build"
            }
        }
        
        stage("Testing code"){
            steps{
                sh "gradle test"
            }
        }
    }
}

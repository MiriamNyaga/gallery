pipeline {
    agent any
    
    stages {
        stage("Cloning repository") {
            steps {
                git branch: 'master', url: 'https://github.com/MiriamNyaga/gallery.git'
            }
        }
        
        stage("Building code") {
            steps {
                sh "./gradlew build"
            }
        }
        
        stage("Testing code") {
            steps {
                sh "./gradlew test"
            }
        }
    }
}

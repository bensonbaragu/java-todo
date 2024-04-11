pipeline {
    agent any 
    tools {
        gradle "gradle"
    }
    stages{
        stage("Clone code into Jenkins container"){
            steps{
                git branch: 'master' , url : 'https://github.com/bensonbaragu/java-todo.git'
            }
        }
        stage ("Gradle build") {
            steps{
                sh 'gradle build'
            }
        }
        stage ("Gradle test") {
            steps{
                sh 'gradle test'
            }
        }
        stage ("Gradle run") {
            steps{
                sh 'gradle run'
            }
        }
    }
}
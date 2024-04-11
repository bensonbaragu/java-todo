pipeline {
    agent any 
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
        Stage ("Gradle run") {
            steps{
                sh 'gradle run'
            }
        }
    }
}
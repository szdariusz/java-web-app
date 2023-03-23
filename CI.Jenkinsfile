pipeline {
    agent any
    stages{
        stage("Clean Up"){
            steps{
                deleteDir()
            }
        }
        stage("Clone Repo"){
            steps{
                sh "git clone https://github.com/szdariusz/java-web-app.git"
            }
        }
        stage("Build"){
            steps{
                dir("java-web-app"){
                    sh "mvn clean install"
                }
            }
        }
        stage("Test"){
            steps{
                dir("java-web-app"){
                    sh "mvn test"
                }
            }
        }
    }
}

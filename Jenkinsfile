pipeline{
    agent any
    stages{
        stage('welcoming'){
            steps{
                sh "echo welcome to jenkins + maven automation"
            }
        }
        stage('build'){
            steps{
                sh "mvn clean package"
            }
        }
        stage('run'){
            steps{
                sh "java -jar target/demo-jenkins-maven-1.0-SNAPSHOT.jar"
            }
        }
    }
    post{
        success{
            echo "build and deployment successful"
        }
        failure{
            echo "build and deployment failed"
        }
    }
}
pipeline{
    agent any
    stages{
        stage{
            steps{
                sh "echo welcome to jenkins + maven automation"
            }
        }
        stage{
            steps{
                sh "mvn clean package"
            }
        }
        stage{
            steps{
                sh "java -jar target/demo-0.0.1-SNAPSHOT.jar"
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
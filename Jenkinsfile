pipeline{

    agent any

// uncomment the following lines by removing /* and */ to enable
    tools{
       maven 'maven' 
    }
   

    stages{
        stage('build-the-app'){
            steps{
                echo 'this is the build job'
                sh 'mvn compile'
            }
        }
        stage('test-the-app'){
            steps{
                echo 'this is the test job'
                sh 'mvn clean test'
            }
        }
        stage('package-the-app'){
            steps{
                echo 'this is the package job'
                sh 'mvn package -DskipTests'
            }
        }
    }
    
    post{
        always{
            echo 'this pipeline has completed...'
        }
        
    }
<<<<<<< HEAD:Jenkinsfile
    
=======

  }
>>>>>>> 456c002d9a827223dbd63b0ec71f7678a755c6b8:Jenkinsfile-template
}

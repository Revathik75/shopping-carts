pipeline{

    agent any

// uncomment the following lines by removing /* and */ to enable
    tools{
       maven 'maven' 
    }
    

    stages{
        stage('build-the-app'){
            steps{
                echo 'this is the first job'
                sh 'mvm compile'
                
            }
        }
        stage('test-the-app'){
            steps{
                echo 'this is the second job'
                sh 'mvm test'

            }
        }
        stage('package-the-app'){
            steps{
                echo 'this is the third job'
                sh 'mvm package'
 
            }
        }
    }
    
    post{
        always{
            echo 'my pipeline has completed...'
        }
        
    }
    
}:wq


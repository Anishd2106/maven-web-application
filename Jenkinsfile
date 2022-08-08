pipeline { 
    agent any  
    stages { 
        stage('Compile stage') { 
            steps { 
                withMaven(Maven : 'Maven 3.8.6') {
                    sh 'mvn clean'
                } 
            }
        }
        stage('Testing stage') { 
            steps { 
                withMaven(Maven : 'Maven 3.8.6') {
                    sh 'mvn test'
                }
            }
        }
        stage('CDeploy stage') { 
            steps { 
                withMaven(Maven : 'Maven 3.8.6') {
                    sh 'mvn deploy'
                }
            }
        }
    }
}

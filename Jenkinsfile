pipeline {
    agent any
    stages {
        
        stage('Build') { 
            steps {
                 sh 'mvn -B -DskipTests clean package' 
            }
        }
     }
 post {
        always {
            emailext body: 'A Test EMail', recipientProviders: [[$class: 'DevelopersRecipientProvider'], [$class: 'RequesterRecipientProvider']], subject: 'Test'
        }
    }
    
}

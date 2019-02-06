pipeline {
    agent any
    stages {
        
        stage('Build') { 
            steps {
                 sh 'mvn -B -DskipTests clean package' 
            }
        }
        
        stage(‘Archive’) {
             when {
                branch ‘*/master’
                  }
                steps {
                archive ‘*/target/**/*’
                junit ‘*/target/surefire-reports/*.xml’

        
    }
}

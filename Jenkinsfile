pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                    bat '''mvn -B -DskipTests clean package'''
                    bat '''echo Maven Build is compleed'''
            }
        }
        stage('Test') {
            steps {
                bat 'mvn test'
                echo "Maven stage compleed."
            }
            
        }
        stage('Deliver') {
            steps {
                bat './jenkins/scripts/deliver'
                echo "Deliver stage compleed."
            }
        }
    }
}

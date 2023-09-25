pipeline {
    agent none
    
    stages {
        stage('Compile on Slave 1') {
            agent { label 'slave-1' }
            steps {
                sh 'mvn clean compile'
            }
        }
        
        stage('Compile on Slave 2') {
            agent { label 'slave-2' }
            steps {
                sh 'mvn clean compile'
            }
        }
        
        stage('Test on Slave 1') {
            agent { label 'slave-1' }
            steps {
                sh 'mvn test'
            }
        }
        
        stage('Test on Slave 2') {
            agent { label 'slave-2' }
            steps {
                sh 'mvn test'
            }
        }
    }
}

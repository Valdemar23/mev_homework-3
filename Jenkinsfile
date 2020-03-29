pipeline {
    agent any 
    stages {
        stage('---clone repo---') { 
            steps {
                sh "git clone https://github.com/Valdemar23/ukrainofobia.git" 
            }
        }
        stage('---cd repo---') { 
            steps {
                sh "cd ukrainofobia" 
            }
        }
        stage('---applied plugin---') {
            steps {
                sh "mvn -N io.takari:maven:wrapper"
            }
        }
        stage('---package---') { 
            steps {
                sh "./mvnw verify" #or "./mvnw package"
            }
        }
        stage('deployment project') { 
            steps {
                sh "java -jar ./target/yoda-master-jedi-1.0-SNAPSHOT.jar"  
            }
        }
    }
}

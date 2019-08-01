pipeline {
    agent any 
    stages {
        stage('clone repo') { 
            steps {
                sh "rm -rf mev_homework-3"
                sh "git clone https://github.com/Valdemar23/mev_homework-3.git" 
            }
        }
        stage('write hello world to the file') { 
            steps {
                sh "echo 'hello world' >> mev_homework-3/empty-file.txt"  
            }
        }
    }
}

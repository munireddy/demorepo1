pipeline {
    agent { label 'slave05' }
    
    stages{
        stage('Checkout') {
            steps {
                echo "B4 Code clone"
                git 'https://github.com/munireddy/demorepo1.git'
                echo "AF Code clone"
            }    
        }
        stage('list') {
            steps {
                echo "In List stage"
                sh 'ls -ltr'
                echo "End of clone stage"
            }    
        }
        stage('Build') {
            steps {
                echo "In build stage"
               gcc file1.c
                echo "End of build stage"
            }    
        }
        stage('Execute') {
            steps {
                echo "In Execute stage"
               ./a.out
                echo "End of Execute stage"
            }    
        }
    }
}

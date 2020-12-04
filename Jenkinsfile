pipeline {
    agent { label 'slave05' }
    // Start of different stages in a apipe line
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
                echo "ENd of clone stage"
            }    
        }
        stage('createFile'){
            steps{
                sh '''touch file2
                echo "Text in file " >> file2.txt'''
            }
        }
        stage('Build') {
            steps {
                echo "In build stage"
                sh 'gcc file1.c'
                echo "End of build stage"
            }    
        }
        stage('Execute') {
            steps {
                echo "In Execute stage"
                sh './a.out'
                echo "End of Execute stage"
            }    
        }
    }
}

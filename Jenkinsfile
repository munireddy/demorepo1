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
                echo "ENd of clone stage"
            }    
        }
    }
}

pipeline {
    agent any
    stage('Hello') 
        echo 'Building...'
        sh 'make'
    }
    stage('Hello') {
        echo 'Testing...'
        sh 'make check || true'
        junit '**/target/*.xml'
    }
    stage('Hello') {
        echo 'Deploying...'
        sh 'make publish'
    }
}

pipeline {
    agent {
        label "demoAgent"
    }
    
    stages {
        stage('git') {
            steps {
                git branch: 'main', url: 'https://github.com/jsjang00/SeleniumProject.git'
            }
        }        
        stage('mvn') {
            steps {
                sh "mvn -Dmaven.test.failure.ignore=true clean test"
            }
        }
    }
}
pipeline {
    agent any

    stages {
        stage('Get_Code') {
            steps {
                git 'https://github.com/AneesRavidKhan/DemoATC.git'
            }
        }
        stage('Build_Code') {
            steps {
                sh 'mvn install'
            }
        }
        stage('Deploy') {
            steps {
                sh 'scp target/DemoATR.war root@3.110.168.37:/var/lib/tomcat9/webapps'
            }
        }
    }
}
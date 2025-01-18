pipeline {
    agent any
    tools{
        maven 'maven-3.6.3'
    }

    stages {
        stage('GIT Clone') {
            steps {
                git credentialsId: 'Github_username_password', url: 'https://github.com/sandeepkumarmekapothula/tomcat-application.git'
            }
        }

        stage('MAVEN Build') {
            steps {
                sh 'mvn clean install'
            }
        }    
    }
}

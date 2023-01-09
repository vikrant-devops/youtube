pipeline {
        agent any

        stages {
            stage('Checkout') {
                steps {
                        checkout scm
                      }}
                stage('Build') {
                   steps {
                          sh '/home/vikrant/Documents/Maven/apache-maven-3.8.6/bin/mvn install'
                         }}
                stage('Deployment'){
                    steps {

                        sh 'sshpass -p "test" scp target/youtube.war test@172.17.0.2:/home/ubuntu/apache-tomcat-9.0.70/webapps'
        }
}}}


pipeline {
    agent { label 'slave01' }
     stages {
        stage('Checkout') {             
            steps {
                sh "rm -rf webdemohost"
                sh "git clone https://github.com/k19-anavak/hello-world-war.git"
            }
        }
           stage('build') {             
            steps {
                sh "cd webdemohost"
                sh "mvn clean package"
                  }
        }
          stage('deploy') {             
            steps {
                sh "whoami"
                sh "cp target/*.war /opt/apache-tomcat-10.1.35/webapps/"              
            }
        }
    }
}

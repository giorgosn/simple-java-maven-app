pipeline {
    agent {
        docker {
            image 'maven:3-alpine' 
            args ' --env DOCKER_CERT_PATH=/certs/client --env DOCKER_TLS_VERIFY=1  -v /root/.m2:/root/.m2' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}

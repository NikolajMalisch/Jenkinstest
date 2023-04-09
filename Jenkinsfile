pipeline {
    agent {
        docker {
            image 'maven:3-alpine' // use a Docker image with Maven pre-installed
            args '-v /root/.m2:/root/.m2' // mount the Maven repository as a volume for caching
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn -B -DskipTests clean package' // build the Maven project, skip tests
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test' // run tests
            }
            post {
                always {
                    junit 'target/surefire-reports/*.xml' // publish JUnit test results
                }
            }
        }
        stage('Deliver') {
            steps {
                sh './jenkins/scripts/deliver.sh' // run a delivery script
            }
        }
    }
}


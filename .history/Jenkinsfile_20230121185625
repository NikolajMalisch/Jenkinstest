pipeline {
 agent any
 stages {
 stage('Build') {
 steps {
 echo “Die Anwendung wird gebaut”
 sh ''mvn package'
 }
 }
 stage('Test') {
 steps {
 echo “Die Anwendung wird getestet”
 sh 'mvn test'
 }
 }
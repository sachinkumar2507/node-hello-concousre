pipeline{
  agent any
   tools { nodejs "Node"}
  stages {
   stage ('parallel build'){
     parallel {
       stage("on linux"){
         agent {label 'slave1'}
     steps{
         sh 'npm install'
         sh 'npm pack'
         echo "congratulation"
      }
    } 
      stage("on Window"){
         agent {label 'slavefor'}
     steps{
         sh 'npm start'
      }
    }
 }
}
 }
}

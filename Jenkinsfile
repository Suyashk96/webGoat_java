pipeline {
  agent any 
  tools {
    maven 'Maven'
  }
  stages {
    stage ('Initialize') {
      steps {
        sh '''
                echo "PATH = ${PATH}"
                echo "M2_HOME = ${M2_HOME}"
            ''' 
      }
    }
    
    stage ('Build') {
      steps {
        sh 'mvn clean install -DskipTests'
      }
    }
    
    stage ('directory') {
      steps {
      sh 'pwd'
       }
    }
  
    
    stage ('check') {
      steps {
         sh 'ls -la'
      }
    }
   }  
}
pipeline {
  agent none
  stages {
    stage('Maven Install') {
      agent {
        docker {
          image 'maven:3.5.0'
        }
      }
      steps {
        sh 'mvn clean install'
      }
    }
    
    
	stage('Sonar Analysis') {
      agent any
      steps {
		
      }
  }
  }
  
  stage('Quality Gate') {
      agent any
      steps {
		
        }
		}
      }
  } 
    
     stage('Artifactory Upload') {
      agent any
      steps {

       
          
        }
        """
        def buildInfo = Artifactory.newBuildInfo() 
        buildInfo.env.capture = true 
        buildInfo=server.upload(uploadSpec) 
        server.publishBuildInfo(buildInfo) 
		}
      }
    }
     
    stage('Docker Build') {
      agent any
      steps {
      sh 'docker stop c_nsingla_java || true && docker rm c_nsingla_java || true'
      
        sh 'docker build -t i_nsingla_java:latest .'
        
        sh 'docker run --name c_nsingla_java -d -p 5085:8080 i_nsingla_java'
        
       
      }
    }
    
    stage('Test Results') {
      agent any
      steps {
       
       
      }
    }
    
    
  }
}


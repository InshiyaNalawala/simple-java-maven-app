pipeline {
    
    agent none
    
   stages {
        
        stage('Build'){
            
            agent {
                label "myslavemaven"
            }
          
          steps {
             
                echo "git downloading..."
                git 'https://github.com/InshiyaNalawala/simple-java-maven-app.git'
                sh 'mvn package'
                sh 'java -jar target/*.jar'
                archiveArtifacts artifacts: 'target/*.jar' , followSymlinks: false
          }
        }
   }
}

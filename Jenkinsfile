pipeline { 
    agent any  
    tools { 
        maven 'maven3' 
        jdk 'jdk8' 
    }
    stages { 
        stage ('Initialize') {
            steps {
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
            }
        }
        stage('Build') { 
            steps { 
               echo 'This is a minimal pipeline.' 
            }
        }
    }
}

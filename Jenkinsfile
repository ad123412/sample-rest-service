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
               echo 'maven will run the junit test and build and create the artifacts'
               bat 'mvn clean package'
            }
            post {
                success {
                    archiveArtifacts artifacts: 'target/**/*.jar', fingerprint: true
                    junit 'target/surefire-reports/**/*.xml'
                }
            }
        }
    }
}

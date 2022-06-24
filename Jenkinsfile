pipeline {
    agent any
    
    
    stages {
        stage ('Initialize') {
            steps {
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                '''
            }
        }
stage('Maven Installation')

{

steps{

echo "Building the checked out project...";

bat "mvn clean install";

}

}

stage('Deploy')

{

steps{

echo "Deploying Project";

}

}

}

}

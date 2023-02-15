pipeline {
agent any
stages {
    stage('Build') {
        steps {
            sh 'g++ -o PES2UG20CS194-1 hello.cpp'
        }
    }
    
    stage('Test') {
        steps {
            sh './PES2UG20CS194-1'
        }
    }
    
    stage('Deploy') {
        steps {
            // deployment code
            echo 'deployment successful'
        }
    }
}

post {
    always {
        script {
            if (currentBuild.result == "FAILURE") {
                echo "Pipeline failed"
            }
        }
    }
}
}

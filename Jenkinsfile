pipeline {
agent any
stages {
    stage('Build') {
        steps {
            sh 'g++ -o pes2ug20cs504-1 hello.cpp'
        }
    }
    
    stage('Test') {
        steps {
            sh './pes2ug20cs504-1'
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

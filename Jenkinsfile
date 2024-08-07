pipeline {
    agent any
    
    stages {
        stage('Hello'){
            steps {
                cleanWs()
                echo 'Building a new laptop ...'
                sh 'pwd'
                sh 'mkdir -p build'
                sh 'touch build/computer.txt'
                sh 'echo "Mainboard" >> build/computer.txt'
                sh 'cat build/computer.txt'
                sh 'echo "Display" >> build/computer.txt'
                sh 'cat build/computer.txt'
                sh 'echo "Keyboard" >> build/computer.txt'
                sh 'cat build/computer.txt'
            }
        }
    }
    
    post {
        success {
            archiveArtifacts artifacts: 'build/**'
        }
        

    }
}

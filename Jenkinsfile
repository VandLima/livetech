pipeline {
    agent {
        docker {
            image 'ruby'
        }
    }

    stages {
        stage('Biuld') {
            steps {
                echo 'Building Resolve dependencies!'
            }
        }
        stage('Teste') {
            steps {
             echo 'Runing regression tests'
            }
        }
        stage('UAT') {
            steps {
                echo 'Wait for user Acceptence'
                input (message: 'Go to prodution', ok: 'Yes')
            }
        }
        stage('Prod') {
            steps {
                echo 'webApp is Ready :)'
            } 
        }
    }
}
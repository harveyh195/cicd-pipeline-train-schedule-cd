pipeline {
    agent any
    options {
       ansiColor('xterm')
    }
    stages {
        stage('Build') {
            steps {
                echo '\033[34mHello\033[0m \033[33mcolorful\033[0m \033[35mworld!\033[0m'
                
            }
        }
        stage('list'){
            steps {
                bat 'dir'
                bat 'echo %cd%'
            }
        }
        stage ('Invoke_pipeline') {
            steps {
                build job: '45', parameters: [
                string(name: 'param1', value: "value1")
                ]
            }
        }
    }
}

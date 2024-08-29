pipeline {
    agent any
    environment {
        name = "Minaxi"
        uname = "sapara"
    }
    parameters {
        string (name :'person', defaultValue : 'XZY', description: 'Who are you?' )
    }
    stages {
        stage ('hello'){
            steps {
                echo "hello word"
                echo "My name is ${name}"
                echo "the name is ${person}"
            }
        }
        stage ('continue?'){
            input {
                message "should we contineu?"
                ok "yes we should"
            }
            steps{
                echo "hi"
            }
        }
         stage ('hi'){
            steps {
                echo "hello word"
                echo "My name is ${uname}"
            }
        }
    }
    post {
        always {
            echo "i will"
        }
        failure {
            echo "fail"
        }
        success {
            echo "done"
        }
    }
}

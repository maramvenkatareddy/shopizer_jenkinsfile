pipeline {
    agent { label 'node' }
    triggers { pollSCM('* * * * *') }
    
    stages {
        stage ('sourcecode') {
            steps {
                git url: 'https://github.com/maramvenkatareddy/shopizer.git',
                    branch: 'master'
            }
        }
        stage ('build the code') {
            steps {
                sh 'mvn package'
            }
        }
    }
}

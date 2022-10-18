pipeline {
    agent { label 'node' }
    triggers { cron('0 5 * * *') }
    
    stages {
        stage ('sourcecode') {
            steps {
                git url: 'https://github.com/maramvenkatareddy/shopizer.git',
                    branch: 'release'
            }
        }
        stage ('build the code') {
            steps {
                sh 'mvn package'
            }
        }
    }
}

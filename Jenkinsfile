pipeline {
    agent none
    parameters {
        string(name: 'environment', defaultValue: 'qa', description: 'Backend environment target. Can be dev, qa, or prod.')
        string(name: 'password', defaultValue: '', description: 'Password for unlocking keychain.')
    }
    stages {
        stage("Build") {
            agent any
            steps {
                script {
                    model = readMavenPom file: 'pom.xml'
                    echo model.dump()
                    value = model.dependencies['dependency.groupId']
                    echo value
                }
            }
        }
        stage("Upload to S3") {
            agent any
            steps {
                echo 'Hello World2'
            }
        }
    }
}

pipeline {
    agent any
    parameters {
        string(name: 'environment', defaultValue: 'qa', description: 'Backend environment target. Can be dev, qa, or prod.')
        string(name: 'password', defaultValue: '', description: 'Password for unlocking keychain.')
    }
    stages {
        stage("Build") {
            when { expression { return true } }
            steps {
                echo 'Hello World1'
            }
            post { 
                always { 
                    echo 'Build Post'
                }
            }
        }
        stage("Upload to S3") {
            when { expression { return true } }
            steps {
                echo 'Hello World2'
            }
            post { 
                always { 
                    echo 'Upload Post'
                }
            }
        }
    }
    post { 
        always { 
            echo 'Global Post'
        }
    }
}

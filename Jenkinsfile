pipeline {
    agent any
    environment{
        name='saim'
    }
    stages {
        stage('test') {
            steps {
                script {
                    
                    bat """
                        echo Build ID: ${env.BUILD_ID}
                        echo Name: ${name}
                        dir
                    """
                    
                }
                echo 'test'
            }
        }
        stage('build') {
            steps {
                echo 'build'
            }
        }
        stage('deploy') {
            steps {
                echo 'deploy on test'
            }
        }
        stage('production') {
            steps {
                echo 'deploy on production'
            }
        }
    }
    post{
        always{
            echo 'I will always run'
        }
        success{
            echo 'I will always run when success'
        }
        failure{
            echo 'I will always run when failure'
        }
    }
}

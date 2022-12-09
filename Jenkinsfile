pipeline{
    agent any
    stages{
        stage('1-Stage1'){
            agent{
                label 'slave1'
            }
            steps{
                sh 'ps -ef'
            }
        }
        stage("2-Stage2){
            agent{
                label 'slave1'
            }
            steps {
                sh 'java -version'
            }
        }
        stage('3-Stage3'){
            agent{
                label 'slave2'
            }
            parallel{
                stage('3-Stage3-1'){
                    steps{
                        echo 'Parallel action1'
                    }
                }
                stage('4-Stage3-2'){
                    steps{
                        echo 'Parallel action2'
                    }
                }
            }
        }
        stage('5-Stage5'){
            agent{
                label 'slave3'
            }
            steps{
                sh 'free -g'
            }
        }
        stage('6-Stage6'){
            agent{
                label 'slave3'
            }
            steps{
                echo 'Welcome to etechApp'
            }
        }
    }
}
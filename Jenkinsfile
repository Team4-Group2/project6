pipeline{
    agent any
    stages{
        stage('1-EngEkong'){
            agent{
                label 'slave1'
            }
            steps{
                sh 'ps -ef'
            }
        }
        stage('2-EngAnakua'){
            agent{
                label 'slave2'
            }
            steps{
                sh 'ps -ef'
            }
        }
    }
}
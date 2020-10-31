pipeline{
    agent any
    stages{
        stage('fetch code'){
            steps{
               git 'https://github.com/kpkk/ACMEBuild.git'
            }
        }
        stage('build'){
            steps{
                bat 'mvn clean install'
            }
        }
    }
    post{
        always{
            emailext body: 'the build status is notified..please check',
            subject: 'test email', 
            to: 'kadarla.pradeep4@gmail.com'
        }
    }
}

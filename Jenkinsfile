pipeline{
    agent any
    stages{
        stage("Build"){
            steps{
                git branch: 'master', changelog: false, credentialsId: 'github-jenkins-access', poll: false, url: 'https://github.com/octobit8-pvt-ltd/django_app_farahzeba.git'
                bat 'builparser.py
'
            }
        }
    }
    post {
        always {
            emailext subject: 'Jenkins Build Notification',
                     body: 'Successfully built post build in jenkins',
                     to: 'zebafarah85@gmail.com ,farah.zeba@octobit8.com'
               }
         } 
        }
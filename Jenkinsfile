@Library('Shared')_
pipeline{
    agent { label 'node1'}
    
    stages{
        stage("Code clone"){
            steps{
                sh "whoami"
            clone("https://github.com/ritikraj096/django-notes-app","main")
            }
        }
        stage("Code Build"){
            steps{
            hello()
            dockerbuild("notes-app","latest")
            }
        }
    
        stage("Deploy"){
            steps{
                deploy()
            }
        }
        
    }
}

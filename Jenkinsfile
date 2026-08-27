@Library('Shared')_
pipeline{
    agent { label 'node1'}
    
    stages{
        stage("Code clone"){
            steps{
                script{
                    clone("https://github.com/ritikraj096/django-notes-app","main")
                }
            }
        }
        stage("Code Build"){
            steps{
                script{
                    hello()
                    dockerbuild("notes-app","latest")
                }
            }
        }
    
        stage("Deploy"){
            steps{
                deploy()
            }
        }
        
    }
}

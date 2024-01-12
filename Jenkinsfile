pipeline
{
    agent any



    stages
    {
        stage('clone')
        {
            steps
            {
                git branch: "main", url: "https://github.com/Sharath-9632904366/my-app.git"
            }
        }    
            stage('clean')
            {
                steps
                {
                    sh "mvn clean"
                }
            }    
                stage('test')
                {
                    steps
                    {
                        sh "mvn test"
                    }
                }    
                    stage("build")
                    {
                        steps
                        {
                            sh "mvn package"
                        }
                    }
         
    }
}    
        
        
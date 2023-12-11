pipeline
{
    agent { label 'demo' }
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
                    stage("deploy")
                    {
                        steps
                        {
                            sh "scp target/app.war gk@172.17.0.3/home/gk/apache-tomcat-9.0.83/webapps"

                        }
                    }
            
         
    }
}    
        
        
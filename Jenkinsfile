pipeline
{
    agent any
   /* tools { 
        maven 'maven1' 
        jdk 'openjdk-11' 
    }*/
    stages
    {         
        stage("Build BE")
        {
           /* agent
            {
                docker
                {
                    image 'maven:3.8-adoptopenjdk-11' 
                    args '-v /root/.m2:/root/.m2' 
                }
            }*/
            
            steps
            {              
                sh "mvn -v"
                
            }
        }
    


    }
        
        post
        {
            always
            {
                cleanWs()                
            }
        }


}

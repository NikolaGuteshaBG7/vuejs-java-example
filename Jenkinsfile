pipeline
{
    agent any
    tools { 
        maven 'maven1' 
        jdk 'java1' 
    }
    stages
    {
        // front end

        stage("Install FE packages")
        {
            steps
            {
                dir("src/main/ui")
                {
                sh 'pwd'
                }
                

                echo "Installing npm packages"
                nodejs('Node16.2.0')
                {
                    sh 'npm install'
                }

            }
        }

        stage("Audit FE")
        {
            steps
            {
                dir("src/main/ui")
                {
                sh 'pwd'
                }
                
                echo "Auditing npm packages"
                nodejs('Node16.2.0')
                {
                    sh 'npm audit'
                }

            }
        }
        
        stage("Test FE")
        {
            steps
            {                 
                echo "Testing......"                
            }
        }

        stage("Build BE")
        {
            agent
            {
                docker
                {
                    image 'maven:3.8.1-adoptopenjdk-11' 
                    args '-v /root/.m2:/root/.m2' 
                }
            }
            
            steps
            {
                sh 'sudo mvn -B -e -X'
            }
        }


    }


}

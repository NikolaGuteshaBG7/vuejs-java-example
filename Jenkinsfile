pipeline
{
    agent any
    tools { 
        maven 'maven1' 
       // jdk 'jdk8' 
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
            steps
            {
                sh 'mvn clean install'
            }
        }


    }


}

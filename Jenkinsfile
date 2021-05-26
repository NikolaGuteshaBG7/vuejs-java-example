pipeline
{
    agent any
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

        stage("Build FE")
        {
            steps
            {
                dir("src/main/ui")
                {
                sh 'pwd'
                }
                
                echo "Building FE app"
                nodejs('Node16.2.0')
                {
                    sh 'npm build'
                }

            }
        }


    }


}

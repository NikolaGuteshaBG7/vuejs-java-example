pipeline
{
    agent any
    stages
    {
        // front end

        stage("Isntall FE packages")
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
                echo "Building FE app"
                nodejs('Node16.2.0')
                {
                    sh 'npm run build'
                }

            }
        }


    }


}

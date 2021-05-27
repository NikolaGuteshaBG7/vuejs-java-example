https://www.youtube.com/watch?v=HaGeSq-SB9E
https://www.jenkins.io/doc/book/pipeline/docker/


Advantages:

Not dependant on the master node's configurations!!!!!!
Add your own!


FORMAT:

 agent 
    { 
        docker
        {
         image "maven:3.6.0-jdk-13"
         label "docker"
        }
    }

DOCKERFILE::::

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


MOUNT FOLDER TO PRESERVE DATA!!!!!!!!
agent 
    { 
        docker
        {
         image "maven:3.6.0-jdk-13"
         args '-v /root/.m2:/root/.m2' 
         }
    } 






DOCKERFILE::::

pipeline
{ 
    agent any
    stages
    {
        stage('continous download')
 	    {
            steps
            {
                git 'https://github.com/Ravichaitanya24/mavennew.git'
            }
        }
        stage('continous build')
        {
            steps
            {
                sh 'mvn package'
            }
        }
        stage('continous deployment')
        {
            steps
            {
                sh 'scp /home/ubuntu/.jenkins/workspace/dev1/webapp/target/webapp.war ubuntu@172.31.32.90:/var/lib/tomcat9/webapps/testapp.war'
            }
        }
       stage('continous testing')
        {
            steps
            {
                 git 'https://github.com/intelliqittrainings/FunctionalTesting.git'
                sh 'java -jar /home/ubuntu/.jenkins/workspace/dev1/testing.jar'
            }
        } 
         stage('continous delivery')
        {
            steps
            {
                sh 'scp /home/ubuntu/.jenkins/workspace/dev1/webapp/target/webapp.war ubuntu@172.31.40.87:/var/lib/tomcat9/prodapp.war'
            }
        }
    }
}

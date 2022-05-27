@Library('mathcalculations')_
pipeline
{
    agent any
    stages
     {
        stage('Continous download_Loans')
        {
            steps
            {
                script
                {
                    cicd.newGit('https://github.com/intelliqittrainings/maven.git')
                }
            }
         }
         stage('continous build_Loans')
         {
             steps
             {
                 script
                 {
                     cicd.newMaven()
                 }
             }
         }
         
    }
}

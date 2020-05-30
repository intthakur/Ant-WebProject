pipeline 
{
    agent any
      stages 
           {
              stage ('Clean work dirs')
                {
                  
                  steps 
                   {
                     withAnt (installation: 'ANT_HOME', jdk: 'localjdk-8') 
                      {
                        sh 'ant info'
                      }
                    }
                 }
                       
                stage ('package')
                  {
                    steps
                      {
                         withAnt (installation: 'ANT_HOME', jdk: 'localjdk-8')
                          {
                            sh 'ant package'
                          }
                       }
                   }
                stage ('archieve')
                  {
                    steps
                      {
                         withAnt (installation: 'ANT_HOME', jdk: 'localjdk-8')
                          {
                            sh 'ant war'
                          }
                       }
                   }
                 
            }
}

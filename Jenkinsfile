pipeline
{
    agent any
    stages
    {
      stage('scm checkout')
      {
          steps {

              git branch: 'master', url: 'https://github.com/intthakur/Ant-WebProject'
          }
      }

      stage('ant build')
      {
           steps{
           withAnt(installation: 'ANT_HOME', jdk: 'localjdk-8') {
                 sh 'ant -f build.xml -v'
}
}
}
}
}

node('built-in') 
{
    // some block
    stage('CD') 
    {
    // some block
    git 'https://github.com/intelliqittrainings/maven.git'
    //git 'https://github.com/devopsakhil5/jenkins-CI-CD-script.git'
    }
    
    stage('CB') 
    {
    // some block
    sh 'mvn package'
    }
    
    stage('CDLY') 
    {
    // some block
    deploy adapters: [tomcat9(credentialsId: '2fdf697b-361c-4d7a-854a-205cf23ff660', path: '', url: 'http://172.31.91.188:8080')], contextPath: 'test', war: '**/*.war'
    }
    
     stage('CT') 
    {
    // some block
    git 'https://github.com/intelliqittrainings/FunctionalTesting.git'
    sh 'java -jar /home/ubuntu/.jenkins/workspace/scripedpipeline1/testing.jar'
    }
    
     stage('CDel') 
    {
    // some block
    input message: 'Need approval of DM!!', submitter: 'Srinivas'
  deploy adapters: [tomcat9(credentialsId: '2fdf697b-361c-4d7a-854a-205cf23ff660', path: '', url: 'http://172.31.29.147:8080')], contextPath: 'prod', war: '**/*.war'
    }
}

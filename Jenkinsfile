pipeline{
    agent any

    tools {
         maven 'MAVEN_HOME'
    }

    stages{
        stage('checkout'){
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'github access', url: 'https://github.com/Humanbeingvish/Helloworld-mvn.git']]])
            }
        }
        stage('Package'){
            steps{
               sh 'mvn package'
            }
        }
    }
}

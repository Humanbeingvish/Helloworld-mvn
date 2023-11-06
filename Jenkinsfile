pipeline{
    agent any

    tools {
         maven 'MAVEN_HOME'
         jdk 'JAVA_Home'
    }

    stages{
        stage('checkout'){
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'github access', url: 'https://github.com/Humanbeingvish/Helloworld-mvn.git']]])
            }
        }
        stage('build'){
            steps{
               sh 'clean install'
            }
        }
    }
}

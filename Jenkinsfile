pipeline{
    agent any

    tools {
         maven 'maven'
         jdk 'JDK'
    }

    stages{
        stage('checkout'){
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'git-cre', url: 'https://github.com/Santhosh-Nagarajan/mave-demo.git']]])
		}
        }
        stage('build'){
            steps{
               sh 'mvn package'
            }
        }
    }
}

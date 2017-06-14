node {
   stage('Prepare') { 
        checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '296cec77-12a9-4979-ae2b-3616c6e0b363', url: 'https://github.com/ianjenkinssem/romannumerals']]])
   }
   
   stage('Test') { 
       sh: 'mvn test'
   }
}

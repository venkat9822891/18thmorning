node('built-in') {
    stage('Download') {
     git branch: 'test', url: 'https://github.com/venkat9822891/18thmorning.git'
                           }
    stage('Convert Artifacts') {
          sh 'mvn package'
                               }
    stage('Deployment')	{		       
    deploy adapters: [tomcat9(credentialsId: '61812315-b402-4f45-8acf-fd266117c279', path: '', url: 'http://172.31.7.78:8080')], contextPath: '/devapps', war: '**/*.war'
    }
}

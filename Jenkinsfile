node {
    stage('"Download git repository"') {
         git branch: 'dev', url: 'https://github.com/clouddevopseng/new-proj-k.git'
     }
     stage('"Covert Artifacts"') {
    sh 'mvn package'
     }
     stage('"Deployment in Environment modified"') {
    deploy adapters: [tomcat9(credentialsId: 'a242f5af-1a2c-4772-b116-cbc1fd0921bb', path: '', url: 'http://172.31.4.208:8080')], contextPath: '/dev-env', war: '**/*.war'
     }
}

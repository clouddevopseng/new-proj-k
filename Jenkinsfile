node {
    stage('"Download git repository"') {
         git branch: 'test', url: 'https://github.com/clouddevopseng/new-proj-k.git'
     }
     stage('"Covert Artifacts"') {
    sh 'mvn package'
     }
     stage('"Deployment in Environment"') {
    deploy adapters: [tomcat9(credentialsId: '55783947-24c7-46e2-ac64-4db76c24ddaf', path: '', url: 'http://172.31.14.137:8080')], contextPath: '/test-env', war: '**/*.war'
     }
}

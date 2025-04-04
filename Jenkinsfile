node {
    stage('"Download git repository"') {
         git branch: 'qa', url: 'https://github.com/clouddevopseng/new-proj-k.git'
     }
     stage('"Covert Artifacts"') {
    sh 'mvn package'
     }
     stage('"Deployment in Environment"') {
    deploy adapters: [tomcat9(credentialsId: 'ec5a0d55-fcbc-456a-9250-4efe5a41623b', path: '', url: 'http://172.31.7.27:8080')], contextPath: '/qa-env', war: '**/*.war'
     }
}

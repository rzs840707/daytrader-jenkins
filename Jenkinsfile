podTemplate(cloud: 'default', label: 'mypod', containers: [
    containerTemplate(name: 'maven', image: 'maven:3.3.9-jdk-8-alpine', ttyEnabled: true, command: 'cat')
  ]) {

    node('mypod') {
        stage('Get a Maven project') {
            sh 'env'
            sh 'export http_proxy=http://172.21.254.254:3128/'
            sh 'export https_proxy=http://172.21.254.254:3128/'
            sh 'git config --global http.proxy http://172.21.254.254:3128'
            sh 'git config --global https.proxy http://172.21.254.254:3128'
            
            sh 'mvn -B clean install'
                     
        }
    }
}

node('mypod') {
    stage('Get a Maven project') {
        sh 'env'
        sh 'export http_proxy=http://172.21.254.254:3128/'
        sh 'export https_proxy=http://172.21.254.254:3128/'
        sh 'git config --global http.proxy http://172.21.254.254:3128'
        checkout scm
        def MAVEN_BUILD=tool name: 'Maven 3.5.0', type: 'hudson.tasks.Maven$MavenInstallation'
        sh 'mvn --help'
    }
}

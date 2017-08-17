node {
    dir('build') {
        sh 'env'
    println "Node env:"
    println env.getEnvironment()
        stage('Checkout') {
            checkout scm
        }

        def WORK_DIR=pwd()

        stage('Build / Unit Test') {
            def MAVEN_BUILD=tool name: 'Maven 3.3.9', type: 'hudson.tasks.Maven$MavenInstallation'
            echo "Driving build and unit tests using Maven $MAVEN_BUILD"
            def JAVA8_HOME=tool name: 'JDK 1.8 (latest)', type: 'hudson.model.JDK'
            echo "Running build and unit tests with Java $JAVA8_HOME"
        }
    }
}

node {
    stage('Checkout') {
        checkout scm
    }

    stage('Build Java') {
        sh './gradlew'
    }

    stage('Build Cpp') {
        sh 'cppbuild/cppbuild'
    }
}

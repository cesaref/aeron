node {
    stage('Checkout') {
        checkout scm
    }

    stage('Build Cpp') {
        sh 'cppbuild/cppbuild'
    }
}

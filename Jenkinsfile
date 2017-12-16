// Define the lables that we want to run the build on in parallel
// Setup jenkins nodes with these lables defined
def labels = ['linux', 'osx']

def builders = [:]

for (x in labels) {
    def label = x

    builders[label] =  {

        node(label) {
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
    }
}

parallel builders

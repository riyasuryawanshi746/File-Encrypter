pipeline {
agent any
stages {

stage('Build') {
steps {
sh '''
echo "Building Java project..."
cd "Password Protection"
mkdir -p build
javac -d build src/*.java
'''
}
}

stage('Test') {
steps {
sh '''
echo "Running Tests..."
'''
}
}

stage('Deploy') {
steps {
sh '''
echo "Packaging Application"
cd "Password Protection"
jar cf FileEncrypter.jar -C build .
'''
}
}
}
}

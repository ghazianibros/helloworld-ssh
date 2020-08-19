node{
    stage('SCM Checkout'){
        git 'https://github.com/ghazianibros/helloworld-maven.git'
    }
    stage('Compile-Package'){
        sh 'mvn clean package'
    }
}
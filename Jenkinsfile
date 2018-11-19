node{
  stage('Build'){
    echo "Hello! Building form file"
    checkout scm
    sh 'javac MainClass.java'
  }

  stage('Test'){
    echo "Testing"
    sh 'java MainClass'
  }
}

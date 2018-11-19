node{
  stage('Build'){
    echo "Hello! Building form file"
    sh 'cd MyJenTest'
    sh 'javac MainClass.java'
  }

  stage('Test'){
    echo "Testing"
    sh 'java MainClass'
  }
}

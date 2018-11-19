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

  stage('Deploy'){
    echo "Deploying"
    sh 'git checkout deploy-branch'
    sh 'git merge origin/master'
    sh 'git push http://ahkhawer:Mistri521@github.com/ahkhawer/MyJenTest.git origin deploy-branch'
    echo 'Code is deployed to the branch'
  }
}

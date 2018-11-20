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
    sh 'git add --all'
    sh 'git push origin master'
    sh 'git checkout deploy-branch-three'
    sh 'git config user.name "ahkhawer"'
    sh 'git config user.password "Mistri521"'
    sh 'git add --all'
    sh 'git config user.name'
    //sh 'git commit --author="ahkhawer <ahjavediqbal@gmail.com>" -m "Jenkinfile commit"'
    sh 'git commit -m "Jenkinfile commit"'
    //sh 'git push https://ahjavediqbal@gmail.com:Mistri521@github.com/ahkhawer/MyJenTest.git origin deploy-branch-three'
    sh 'git push origin deploy-branch-three'
    echo 'Code is deployed to the branch'
  }
}

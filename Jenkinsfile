node{
  stage('Build'){
    echo "Hello! Building form file"
    checkout scm
    echo "BUILD_NUMBER" :: $BUILD_NUMBER
    echo "BUILD_ID" :: $BUILD_ID
    echo "BUILD_DISPLAY_NAME" :: $BUILD_DISPLAY_NAME
    echo "JOB_NAME" :: $JOB_NAME
    echo "JOB_BASE_NAME" :: $JOB_BASE_NAME
    echo "BUILD_TAG" :: $BUILD_TAG
    echo "EXECUTOR_NUMBER" :: $EXECUTOR_NUMBER
    echo "NODE_NAME" :: $NODE_NAME
    echo "NODE_LABELS" :: $NODE_LABELS
    echo "WORKSPACE" :: $WORKSPACE
    echo "JENKINS_HOME" :: $JENKINS_HOME
    echo "JENKINS_URL" :: $JENKINS_URL
    echo "BUILD_URL" ::$BUILD_URL
    echo "JOB_URL" :: $JOB_URL
    sh 'javac MainClass.java'
  }

  stage('Test'){
    echo "Testing"
    sh 'java MainClass'
  }

  stage('Deploy'){
    echo "Deploying"
    sh 'git checkout -f deploy-branch'
    sh 'git merge origin/master'
    sh 'git config user.name "ahkhawer"'
    sh 'git config user.password "Mistri521"'
    sh 'git add --all'
    sh 'git commit --author="ahkhawer <ahjavediqbal@gmail.com>" -m "Jenkinfile commit"'
    sh 'git push https://ahjavediqbal@gmail.com:Mistri521@github.com/ahkhawer/MyJenTest.git origin master'
    echo 'Code is deployed to the branch'
  }
}

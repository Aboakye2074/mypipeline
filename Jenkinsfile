pipeline {

environment {

BUILD_SCRIPTS_GIT="http://http://18.220.56.111:8080//scm/~afia/mypipeline.git"

BUILD_SCRIPTS='mypipeline'

BUILD_HOME='/var/lib/jenkins/workspace'

}

agent any

stages {

stage('Checkout: Code') {

steps {

sh "mkdir -p $WORKSPACE/repo;\

git config --global user.email 'tonboazz2003@yahoo.com';\

git config --global user.name 'Aboakye2074';\

git config --global push.default simple;\

git clone $BUILD_SCRIPTS_GIT repo/$BUILD_SCRIPTS"

sh "chmod -R +x $WORKSPACE/repo/$BUILD_SCRIPTS"

}

}

stage('Yum: Updates') {

steps {

sh "sudo chmod +x $WORKSPACE/repo/$BUILD_SCRIPTS/scripts/update.sh"

sh "sudo $WORKSPACE/repo/$BUILD_SCRIPTS/scripts/update.sh"



}

}

post {

always {

cleanWs()

}

}

}

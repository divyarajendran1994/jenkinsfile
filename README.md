# jenkinsfile
node{
stage('SCM Checkout')
{
git 'https://github.com/javahometech/my-app'}
stage('compile-package'){
def mvnhome = tool name: 'maven-3', type: 'maven'
sh "${mvnHome}/bin/mvn package"
}
}

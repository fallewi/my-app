node
{
stage ('checkout mon repo')
{
    git 'https://github.com/fallewi/my-app.git'
}
stage ('build le projet ')
{
   def  mvnhome = tool name: 'maven 3.6.3', type: 'maven'
   def  mvnCMD = "${mvnhome}/bin/mvn"
   sh     "${mvnCMD}  clean package"
}
stage ('Build l\'image avec docker ')
{
    sh "docker build -t fallewi/my-app:v1 ."
}
}

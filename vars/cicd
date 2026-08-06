def git Download (repo)
{
    git"https://github.com/IntelliqDevops/${repo}.git"
}
def build artifact()
{
    sh 'mvn package'
}
def deploy tomcat(jobname,ip,context)
{
    sh"scp/var/lib/jenkins/workspace/${jobname}/webapp/target/webapp.war ubuntu@${ip}:/var/lib/tomcat10/webapps/${context}.war"
}
def run selenium(jobname)
{
    sh"java -jar /var/lib/jenkins/workspace/${jobname}/testing.jar"
}

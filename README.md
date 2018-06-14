# Hello World application

Sample Grails 2.5.6 application to reproduce GraalVM issue.

## Requirements:

* [GraalVM](https://github.com/oracle/graal/releases)
* [Grails 2.5.6](http://grails.org/download.html)

## Steps:

* clone this repository
* cd `helloworld`
* `export JAVA_HOME=/opt/graalvm`
* `/opt/graalvm/bin/java -XX:-UseJVMCIClassLoader -Dgrails.home=/opt/sdkman/candidates/grails/current -Dtools.jar=/opt/graalvm/lib/tools.jar -Dgroovy.starter.conf=/opt/sdkman/candidates/grails/current/conf/groovy-starter.conf "-Dspringloaded=profile=grails;cacheDir=." -Dfile.encoding=UTF-8 -classpath /opt/sdkman/candidates/grails/current/lib/org.codehaus.groovy/groovy-all/jars/groovy-all-2.4.10.jar:/opt/sdkman/candidates/grails/current/dist/grails-bootstrap-2.5.6.jar org.codehaus.groovy.grails.cli.support.GrailsStarter --main org.codehaus.groovy.grails.cli.GrailsScriptRunner --conf /opt/sdkman/candidates/grails/current/conf/groovy-starter.conf run-app`

*Note:* SDKMAN installed in `/opt`; Groovy `2.4.10` used.

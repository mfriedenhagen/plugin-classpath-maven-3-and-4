# plugin-classpath-maven-3-and-4

Difference between Maven 3 and 4 concerning plugin classpath

See https://lists.apache.org/thread.html/r5b843d3979461fe4dfae5da9ee573f3ebd3292518895180ad3d62beb%40%3Cdev.maven.apache.org%3E 
for the discussion 

Running `mvn -q clean verify` with Maven 3.6.3 succeeds while with Maven 4 since
[619973b91cff5af7b5695bda11761a982a159349](https://github.com/apache/maven/commit/619973b91cff5af7b5695bda11761a982a159349) 
this breaks.

```
Apache Maven 4.0.0-alpha-1-SNAPSHOT (619973b91cff5af7b5695bda11761a982a159349)
Maven home: /tmp/apache-maven-4.0.0-alpha-1-SNAPSHOT
Java version: 1.8.0_282, vendor: AdoptOpenJDK, runtime: /Library/Java/JavaVirtualMachines/adoptopenjdk-8.jdk/Contents/Home/jre
Default locale: de_DE, platform encoding: UTF-8
OS name: "mac os x", version: "10.16", arch: "x86_64", family: "mac"
[ERROR] Failed to execute goal net.rumati.maven.plugins:velocity-maven-plugin:0.3.1:velocity (default-velocity) on project plugin-classpath-maven-3-and-4: Error processing template: /net/oneandone/maven/poms/fossconfigs/jenkins-description.html.vm (No such file or directory) -> [Help 1]
[ERROR]
[ERROR] To see the full stack trace of the errors, re-run Maven with the '-e' switch.
[ERROR] Re-run Maven using the '-X' switch to enable full debug logging.
[ERROR]
[ERROR] For more information about the errors and possible solutions, please read the following articles:
[ERROR] [Help 1] http://cwiki.apache.org/confluence/display/MAVEN/MojoExecutionException
```


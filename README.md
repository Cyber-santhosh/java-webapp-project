My console output for for the jenkins multiagent running of JAVA springboot application 


Started by user DevOps Administrator
[Pipeline] Start of Pipeline
[Pipeline] node
Running on Salve_Dev in /home/devopsadmin/workspace/Java-Loksai
[Pipeline] {
[Pipeline] withEnv
[Pipeline] {
[Pipeline] stage
[Pipeline] { (SCM Checkout)
[Pipeline] git
The recommended git tool is: NONE
No credentials specified
Fetching changes from the remote Git repository
Checking out Revision 221cb07275dfa5d3fc1cefe9b5cf7a2f36a0c6f8 (refs/remotes/origin/master)
Commit message: "Update index.html"
 > git rev-parse --resolve-git-dir /home/devopsadmin/workspace/Java-Loksai/.git # timeout=10
 > git config remote.origin.url https://github.com/Cyber-santhosh/java-webapp-project.git # timeout=10
Fetching upstream changes from https://github.com/Cyber-santhosh/java-webapp-project.git
 > git --version # timeout=10
 > git --version # 'git version 2.53.0'
 > git fetch --tags --force --progress -- https://github.com/Cyber-santhosh/java-webapp-project.git +refs/heads/*:refs/remotes/origin/* # timeout=10
 > git rev-parse refs/remotes/origin/master^{commit} # timeout=10
 > git config core.sparsecheckout # timeout=10
 > git checkout -f 221cb07275dfa5d3fc1cefe9b5cf7a2f36a0c6f8 # timeout=10
 > git branch -a -v --no-abbrev # timeout=10
 > git branch -D master # timeout=10
 > git checkout -b master 221cb07275dfa5d3fc1cefe9b5cf7a2f36a0c6f8 # timeout=10
 > git rev-list --no-walk 221cb07275dfa5d3fc1cefe9b5cf7a2f36a0c6f8 # timeout=10
[Pipeline] }
[Pipeline] // stage
[Pipeline] stage
[Pipeline] { (Build Artifacts)
[Pipeline] sh
+ mvn clean package
[[1;34mINFO[m] Scanning for projects...
[[1;34mINFO[m] 
[[1;34mINFO[m] [1m--------------------------< [0;36mcom.loksai:demo[0;1m >---------------------------[m
[[1;34mINFO[m] [1mBuilding demo 1.0-SNAPSHOT[m
[[1;34mINFO[m]   from pom.xml
[[1;34mINFO[m] [1m--------------------------------[ war ]---------------------------------[m
[[1;34mINFO[m] 
[[1;34mINFO[m] [1m--- [0;32mclean:3.3.2:clean[m [1m(default-clean)[m @ [36mdemo[0;1m ---[m
[[1;34mINFO[m] Deleting /home/devopsadmin/workspace/Java-Loksai/target
[[1;34mINFO[m] 
[[1;34mINFO[m] [1m--- [0;32mresources:3.3.1:resources[m [1m(default-resources)[m @ [36mdemo[0;1m ---[m
[[1;34mINFO[m] Copying 1 resource from src/main/resources to target/classes
[[1;34mINFO[m] Copying 0 resource from src/main/resources to target/classes
[[1;34mINFO[m] 
[[1;34mINFO[m] [1m--- [0;32mcompiler:3.11.0:compile[m [1m(default-compile)[m @ [36mdemo[0;1m ---[m
[[1;34mINFO[m] Changes detected - recompiling the module! :source
[[1;34mINFO[m] Compiling 2 source files with javac [debug release 17] to target/classes
[[1;34mINFO[m] 
[[1;34mINFO[m] [1m--- [0;32mresources:3.3.1:testResources[m [1m(default-testResources)[m @ [36mdemo[0;1m ---[m
[[1;34mINFO[m] skip non existing resourceDirectory /home/devopsadmin/workspace/Java-Loksai/src/test/resources
[[1;34mINFO[m] 
[[1;34mINFO[m] [1m--- [0;32mcompiler:3.11.0:testCompile[m [1m(default-testCompile)[m @ [36mdemo[0;1m ---[m
[[1;34mINFO[m] Changes detected - recompiling the module! :dependency
[[1;34mINFO[m] Compiling 1 source file with javac [debug release 17] to target/test-classes
[[1;34mINFO[m] 
[[1;34mINFO[m] [1m--- [0;32msurefire:3.1.2:test[m [1m(default-test)[m @ [36mdemo[0;1m ---[m
[[1;34mINFO[m] Using auto detected provider org.apache.maven.surefire.junitplatform.JUnitPlatformProvider
[[1;34mINFO[m] 
[[1;34mINFO[m] -------------------------------------------------------
[[1;34mINFO[m]  T E S T S
[[1;34mINFO[m] -------------------------------------------------------
[[1;34mINFO[m] Running com.loksai.demo.[1mDemoApplicationTests[m
12:34:14.900 [main] INFO org.springframework.test.context.support.AnnotationConfigContextLoaderUtils -- Could not detect default configuration classes for test class [com.loksai.demo.DemoApplicationTests]: DemoApplicationTests does not declare any static, non-private, non-final, nested classes annotated with @Configuration.
12:34:15.054 [main] INFO org.springframework.boot.test.context.SpringBootTestContextBootstrapper -- Found @SpringBootConfiguration com.loksai.demo.DemoApplication for test class com.loksai.demo.DemoApplicationTests

  .   ____          _            __ _ _
 /\\ / ___'_ __ _ _(_)_ __  __ _ \ \ \ \
( ( )\___ | '_ | '_| | '_ \/ _` | \ \ \ \
 \\/  ___)| |_)| | | | | || (_| |  ) ) ) )
  '  |____| .__|_| |_|_| |_\__, | / / / /
 =========|_|==============|___/=/_/_/_/
 :: Spring Boot ::                (v3.2.3)

2026-07-06T12:34:15.671Z  INFO 14159 --- [           main] com.loksai.demo.DemoApplicationTests     : Starting DemoApplicationTests using Java 17.0.19 with PID 14159 (started by devopsadmin in /home/devopsadmin/workspace/Java-Loksai)
2026-07-06T12:34:15.677Z  INFO 14159 --- [           main] com.loksai.demo.DemoApplicationTests     : No active profile set, falling back to 1 default profile: "default"
2026-07-06T12:34:17.239Z  INFO 14159 --- [           main] o.s.b.a.w.s.WelcomePageHandlerMapping    : Adding welcome page: ServletContext resource [/index.html]
2026-07-06T12:34:17.683Z  INFO 14159 --- [           main] com.loksai.demo.DemoApplicationTests     : Started DemoApplicationTests in 2.437 seconds (process running for 3.828)
OpenJDK 64-Bit Server VM warning: Sharing is only supported for boot loader classes because bootstrap classpath has been appended
[[1;34mINFO[m] [1;32mTests run: [0;1;32m1[m, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 4.084 s -- in com.loksai.demo.[1mDemoApplicationTests[m
[[1;34mINFO[m] 
[[1;34mINFO[m] Results:
[[1;34mINFO[m] 
[[1;34mINFO[m] [1;32mTests run: 1, Failures: 0, Errors: 0, Skipped: 0[m
[[1;34mINFO[m] 
[[1;34mINFO[m] 
[[1;34mINFO[m] [1m--- [0;32mwar:3.4.0:war[m [1m(default-war)[m @ [36mdemo[0;1m ---[m
[[1;34mINFO[m] Packaging webapp
[[1;34mINFO[m] Assembling webapp [demo] in [/home/devopsadmin/workspace/Java-Loksai/target/demo-1.0-SNAPSHOT]
[[1;34mINFO[m] Processing war project
[[1;34mINFO[m] Copying webapp resources [/home/devopsadmin/workspace/Java-Loksai/src/main/webapp]
[[1;34mINFO[m] Building war: /home/devopsadmin/workspace/Java-Loksai/target/demo-1.0-SNAPSHOT.war
[[1;34mINFO[m] 
[[1;34mINFO[m] [1m--- [0;32mspring-boot:3.2.3:repackage[m [1m(repackage)[m @ [36mdemo[0;1m ---[m
[[1;34mINFO[m] Replacing main artifact /home/devopsadmin/workspace/Java-Loksai/target/demo-1.0-SNAPSHOT.war with repackaged archive, adding nested dependencies in BOOT-INF/.
[[1;34mINFO[m] The original artifact has been renamed to /home/devopsadmin/workspace/Java-Loksai/target/demo-1.0-SNAPSHOT.war.original
[[1;34mINFO[m] [1m------------------------------------------------------------------------[m
[[1;34mINFO[m] [1;32mBUILD SUCCESS[m
[[1;34mINFO[m] [1m------------------------------------------------------------------------[m
[[1;34mINFO[m] Total time:  12.141 s
[[1;34mINFO[m] Finished at: 2026-07-06T12:34:21Z
[[1;34mINFO[m] [1m------------------------------------------------------------------------[m
[Pipeline] }
[Pipeline] // stage
[Pipeline] stage
[Pipeline] { (Deploy into QA server)
[Pipeline] sshPublisher
SSH: Connecting from host [ip-172-31-1-114]
SSH: Connecting with configuration [QA server] ...
[Pipeline] }
[Pipeline] // stage
[Pipeline] }
[Pipeline] // withEnv
[Pipeline] }
[Pipeline] // node
[Pipeline] End of Pipeline
Finished: SUCCESS

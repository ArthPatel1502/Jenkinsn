Started by user Arth Patel
Obtained multi_stage_multi_agent/Jenkinsfile from git https://github.com/ArthPatel1502/Jenkins
[Pipeline] Start of Pipeline
[Pipeline] stage
[Pipeline] { (Back-end)
[Pipeline] node
Running on Jenkins in /var/lib/jenkins/workspace/first_pipeline
[Pipeline] {
[Pipeline] checkout
Selected Git installation does not exist. Using Default
The recommended git tool is: NONE
No credentials specified
 > git rev-parse --resolve-git-dir /var/lib/jenkins/workspace/first_pipeline/.git # timeout=10
Fetching changes from the remote Git repository
 > git config remote.origin.url https://github.com/ArthPatel1502/Jenkins # timeout=10
Fetching upstream changes from https://github.com/ArthPatel1502/Jenkins
 > git --version # timeout=10
 > git --version # 'git version 2.53.0'
 > git fetch --tags --force --progress -- https://github.com/ArthPatel1502/Jenkins +refs/heads/*:refs/remotes/origin/* # timeout=10
 > git rev-parse refs/remotes/origin/main^{commit} # timeout=10
Checking out Revision 956d9d8fe00e455a1ca9f2862e9f250af6977607 (refs/remotes/origin/main)
 > git config core.sparsecheckout # timeout=10
 > git checkout -f 956d9d8fe00e455a1ca9f2862e9f250af6977607 # timeout=10
Commit message: "Create README for multi stage multi agent"
 > git rev-list --no-walk bfaf6285e335d84565bfed63601b347e6418dc33 # timeout=10
[Pipeline] withEnv
[Pipeline] {
[Pipeline] isUnix
[Pipeline] withEnv
[Pipeline] {
[Pipeline] sh
+ docker inspect -f . maven:3.8.1-adoptopenjdk-11

error: no such object: maven:3.8.1-adoptopenjdk-11
[Pipeline] isUnix
[Pipeline] withEnv
[Pipeline] {
[Pipeline] sh
+ docker pull maven:3.8.1-adoptopenjdk-11
3.8.1-adoptopenjdk-11: Pulling from library/maven
a18abadafb9a: Pulling fs layer
34d7b43f221b: Pulling fs layer
16ec32c2132b: Pulling fs layer
3f63509f5b97: Pulling fs layer
20904a3b2df7: Pulling fs layer
a1931e18ae45: Pulling fs layer
fb5c0685f15f: Pulling fs layer
a18abadafb9a: Download complete
fb5c0685f15f: Download complete
20904a3b2df7: Download complete
3f63509f5b97: Download complete
16ec32c2132b: Download complete
a1931e18ae45: Download complete
16ec32c2132b: Pull complete
34d7b43f221b: Download complete
3f63509f5b97: Pull complete
34d7b43f221b: Pull complete
a1931e18ae45: Pull complete
20904a3b2df7: Pull complete
a18abadafb9a: Pull complete
fb5c0685f15f: Pull complete
Digest: sha256:143ff7942b5ef5a004252405a31fa2813dfa438f08494fad1757029de5f64082
Status: Downloaded newer image for maven:3.8.1-adoptopenjdk-11
docker.io/library/maven:3.8.1-adoptopenjdk-11
[Pipeline] }
[Pipeline] // withEnv
[Pipeline] }
[Pipeline] // withEnv
[Pipeline] withDockerContainer
Jenkins does not seem to be running inside a container
$ docker run -t -d -u 105:109 -w /var/lib/jenkins/workspace/first_pipeline -v /var/lib/jenkins/workspace/first_pipeline:/var/lib/jenkins/workspace/first_pipeline:rw,z -v /var/lib/jenkins/workspace/first_pipeline@tmp:/var/lib/jenkins/workspace/first_pipeline@tmp:rw,z -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** maven:3.8.1-adoptopenjdk-11 cat
$ docker top 65d698cf72775bc49b9b50c8d436c3288b7cacaff5f00a6f3fcab914313723b7 -eo pid,comm
[Pipeline] {
[Pipeline] sh
+ mvn --version
Apache Maven 3.8.1 (05c21c65bdfed0f71a2f2ada8b84da59348c4c5d)
Maven home: /usr/share/maven
Java version: 11.0.11, vendor: AdoptOpenJDK, runtime: /opt/java/openjdk
Default locale: en_US, platform encoding: UTF-8
OS name: "linux", version: "7.0.0-1006-aws", arch: "amd64", family: "unix"
[Pipeline] }
$ docker stop --time=1 65d698cf72775bc49b9b50c8d436c3288b7cacaff5f00a6f3fcab914313723b7
$ docker rm -f --volumes 65d698cf72775bc49b9b50c8d436c3288b7cacaff5f00a6f3fcab914313723b7
[Pipeline] // withDockerContainer
[Pipeline] }
[Pipeline] // withEnv
[Pipeline] }
[Pipeline] // node
[Pipeline] }
[Pipeline] // stage
[Pipeline] stage
[Pipeline] { (Front-end)
[Pipeline] node
Running on Jenkins in /var/lib/jenkins/workspace/first_pipeline
[Pipeline] {
[Pipeline] checkout
Selected Git installation does not exist. Using Default
The recommended git tool is: NONE
No credentials specified
 > git rev-parse --resolve-git-dir /var/lib/jenkins/workspace/first_pipeline/.git # timeout=10
Fetching changes from the remote Git repository
 > git config remote.origin.url https://github.com/ArthPatel1502/Jenkins # timeout=10
Fetching upstream changes from https://github.com/ArthPatel1502/Jenkins
 > git --version # timeout=10
 > git --version # 'git version 2.53.0'
 > git fetch --tags --force --progress -- https://github.com/ArthPatel1502/Jenkins +refs/heads/*:refs/remotes/origin/* # timeout=10
 > git rev-parse refs/remotes/origin/main^{commit} # timeout=10
Checking out Revision 956d9d8fe00e455a1ca9f2862e9f250af6977607 (refs/remotes/origin/main)
 > git config core.sparsecheckout # timeout=10
 > git checkout -f 956d9d8fe00e455a1ca9f2862e9f250af6977607 # timeout=10
Commit message: "Create README for multi stage multi agent"
[Pipeline] withEnv
[Pipeline] {
[Pipeline] isUnix
[Pipeline] withEnv
[Pipeline] {
[Pipeline] sh
+ docker inspect -f . node:16-alpine
.
[Pipeline] }
[Pipeline] // withEnv
[Pipeline] withDockerContainer
Jenkins does not seem to be running inside a container
$ docker run -t -d -u 105:109 -w /var/lib/jenkins/workspace/first_pipeline -v /var/lib/jenkins/workspace/first_pipeline:/var/lib/jenkins/workspace/first_pipeline:rw,z -v /var/lib/jenkins/workspace/first_pipeline@tmp:/var/lib/jenkins/workspace/first_pipeline@tmp:rw,z -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** node:16-alpine cat
$ docker top d77049997f28308d4eb85f7245025e8acfd83a94c68e8a3cfa1fc89e2a4c76ee -eo pid,comm
[Pipeline] {
[Pipeline] sh
+ node --version
v16.20.2
[Pipeline] }
$ docker stop --time=1 d77049997f28308d4eb85f7245025e8acfd83a94c68e8a3cfa1fc89e2a4c76ee
$ docker rm -f --volumes d77049997f28308d4eb85f7245025e8acfd83a94c68e8a3cfa1fc89e2a4c76ee
[Pipeline] // withDockerContainer
[Pipeline] }
[Pipeline] // withEnv
[Pipeline] }
[Pipeline] // node
[Pipeline] }
[Pipeline] // stage
[Pipeline] End of Pipeline
Finished: SUCCESS

Started by user Arth Patel
Obtained first_pipeline/Jenkinsfile from git https://github.com/ArthPatel1502/Jenkins
[Pipeline] Start of Pipeline
[Pipeline] node
Still waiting to schedule task
Waiting for next available executor
Pausing (shutting down)
Resuming build at Fri Jul 24 12:37:24 UTC 2026 after Jenkins restart
Ready to run at Fri Jul 24 12:37:24 UTC 2026
Running on Jenkins in /var/lib/jenkins/workspace/first_pipeline
[Pipeline] {
[Pipeline] stage
[Pipeline] { (Declarative: Checkout SCM)
[Pipeline] checkout
Selected Git installation does not exist. Using Default
The recommended git tool is: NONE
No credentials specified
Cloning the remote Git repository
Cloning repository https://github.com/ArthPatel1502/Jenkins
 > git init /var/lib/jenkins/workspace/first_pipeline # timeout=10
Fetching upstream changes from https://github.com/ArthPatel1502/Jenkins
 > git --version # timeout=10
 > git --version # 'git version 2.53.0'
 > git fetch --tags --force --progress -- https://github.com/ArthPatel1502/Jenkins +refs/heads/*:refs/remotes/origin/* # timeout=10
 > git config remote.origin.url https://github.com/ArthPatel1502/Jenkins # timeout=10
 > git config --add remote.origin.fetch +refs/heads/*:refs/remotes/origin/* # timeout=10
Avoid second fetch
 > git rev-parse refs/remotes/origin/main^{commit} # timeout=10
Checking out Revision bfaf6285e335d84565bfed63601b347e6418dc33 (refs/remotes/origin/main)
 > git config core.sparsecheckout # timeout=10
 > git checkout -f bfaf6285e335d84565bfed63601b347e6418dc33 # timeout=10
Commit message: "Add Jenkinsfile for Node.js pipeline"
First time build. Skipping changelog.
[Pipeline] }
[Pipeline] // stage
[Pipeline] withEnv
[Pipeline] {
[Pipeline] isUnix
[Pipeline] withEnv
[Pipeline] {
[Pipeline] sh
+ docker inspect -f . node:16-alpine

error: no such object: node:16-alpine
[Pipeline] isUnix
[Pipeline] withEnv
[Pipeline] {
[Pipeline] sh
+ docker pull node:16-alpine
16-alpine: Pulling from library/node
7264a8db6415: Pulling fs layer
eee371b9ce3f: Pulling fs layer
93b3025fe103: Pulling fs layer
d9059661ce70: Pulling fs layer
d9059661ce70: Download complete
7264a8db6415: Download complete
93b3025fe103: Download complete
7264a8db6415: Pull complete
eee371b9ce3f: Download complete
eee371b9ce3f: Pull complete
93b3025fe103: Pull complete
d9059661ce70: Pull complete
Digest: sha256:a1f9d027912b58a7c75be7716c97cfbc6d3099f3a97ed84aa490be9dee20e787
Status: Downloaded newer image for node:16-alpine
docker.io/library/node:16-alpine
[Pipeline] }
[Pipeline] // withEnv
[Pipeline] }
[Pipeline] // withEnv
[Pipeline] withDockerContainer
Jenkins does not seem to be running inside a container
$ docker run -t -d -u 105:109 -w /var/lib/jenkins/workspace/first_pipeline -v /var/lib/jenkins/workspace/first_pipeline:/var/lib/jenkins/workspace/first_pipeline:rw,z -v /var/lib/jenkins/workspace/first_pipeline@tmp:/var/lib/jenkins/workspace/first_pipeline@tmp:rw,z -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** -e ******** node:16-alpine cat
$ docker top a131df7a9a67e86d75112672b17f4602214f277d5a8a196160be690d92524d69 -eo pid,comm
[Pipeline] {
[Pipeline] stage
[Pipeline] { (Test)
[Pipeline] sh
+ node --version
v16.20.2
[Pipeline] }
[Pipeline] // stage
[Pipeline] }
$ docker stop --time=1 a131df7a9a67e86d75112672b17f4602214f277d5a8a196160be690d92524d69
$ docker rm -f --volumes a131df7a9a67e86d75112672b17f4602214f277d5a8a196160be690d92524d69
[Pipeline] // withDockerContainer
[Pipeline] }
[Pipeline] // withEnv
[Pipeline] }
[Pipeline] // node
[Pipeline] End of Pipeline
Finished: SUCCESS

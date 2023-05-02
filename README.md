# DevOps_3rdProj

cd /opt

docker image build -t $JOB_NAME:v1.$BUILD_ID .
docker image tag $JOB_NAME:v1.$BUILD_ID imranawsdevops/$JOB_NAME:v1.$BUILD_ID
docker image tag $JOB_NAME:v1.$BUILD_ID imranawsdevops/$JOB_NAME:latest
docker image push imranawsdevops/$JOB_NAME:v1.$BUILD_ID
docker image push imranawsdevops/$JOB_NAME:latest

docker image rmi $JOB_NAME:v1.$BUILD_ID imranawsdevops/$JOB_NAME:v1.$BUILD_ID imranawsdevops/$JOB_NAME:latest

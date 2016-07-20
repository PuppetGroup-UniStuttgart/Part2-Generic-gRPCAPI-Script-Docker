FROM maven:3.3-jdk-8

# Get sources
RUN git clone --recursive https://github.com/shruthikuki/UniStuttgart-PuppetGroup-gRPC-Generic-DeploymentScript.git
WORKDIR /UniStuttgart-PuppetGroup-gRPC-Generic-DeploymentScript

COPY config.properties /

WORKDIR /UniStuttgart-PuppetGroup-gRPC-Generic-DeploymentScript

CMD cp /api/main.proto /UniStuttgart-PuppetGroup-gRPC-Generic-DeploymentScript/src/main/proto; ls /UniStuttgart-PuppetGroup-gRPC-Generic-DeploymentScript/src/main/proto; mvn clean install; sleep 5s; java -cp /UniStuttgart-PuppetGroup-gRPC-Generic-DeploymentScript/target/DeploymentScript-0.0.1-SNAPSHOT-jar-with-dependencies.jar cloudlab.ops.GenericOpsClient

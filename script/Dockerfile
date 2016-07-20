FROM maven:3.3-jdk-8

# Get sources
RUN git clone --recursive https://github.com/shruthikuki/UniStuttgart-PuppetGroup-gRPC-Generic-DeploymentScript.git
WORKDIR /UniStuttgart-PuppetGroup-gRPC-Generic-DeploymentScript

# Run maven
RUN mvn clean package
RUN ls target

COPY config.properties /

WORKDIR /

CMD sleep 20s; java -cp /UniStuttgart-PuppetGroup-gRPC-Generic-DeploymentScript/target/DeploymentScript-0.0.1-SNAPSHOT-jar-with-dependencies.jar cloudlab.ops.GenericOpsClient

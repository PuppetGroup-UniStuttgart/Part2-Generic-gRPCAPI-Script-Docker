FROM maven:3.3-jdk-8

# Get sources
RUN git clone --recursive https://github.com/shruthikuki/UniStuttgart-PuppetGroup-gRPCGeneric.git
WORKDIR /UniStuttgart-PuppetGroup-gRPCGeneric

# Run maven
RUN mvn clean package

RUN ls target
COPY credentials /root/.aws/credentials
COPY main.proto /api/main.proto

WORKDIR /

VOLUME /api
CMD java -cp /UniStuttgart-PuppetGroup-gRPCGeneric/target/gRPCGeneric-0.0.1-SNAPSHOT-jar-with-dependencies.jar cloudlab.ops.GenericOpsServer

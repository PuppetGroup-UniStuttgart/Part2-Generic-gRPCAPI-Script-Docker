# Part2-Generic-gRPCAPI-Script-Docker

The docker compose bundle runs two containers:

1. grpc container: Runs the Generic Grpc server and responsible for sharing the main.proto file using volumes  
2. script container: Runs the script to access the Generic gRPC API.  
This script deploys MySQL into the EC2 instance


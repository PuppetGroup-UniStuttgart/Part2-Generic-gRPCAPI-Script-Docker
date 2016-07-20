# Part2-Generic-gRPCAPI-Script-Docker

The docker compose bundle runs two containers:

grpc container which runs the Generic Grpc server and responsible for sharing the main.proto file using volumes and the other script container runs the script to access the Generic gRPC API.  
This script deploys MySQL into the EC2 instance


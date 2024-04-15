Overview:
            In this project, I designed and implemented a multi-VPC architecture with both public and private subnets. The goal was to create a network environment that allows secure communication between EC2 instances while ensuring internet access for specific resources.

Key Components:
VPCs:
    Created three separate VPCs to isolate network traffic.
    Each VPC contains one public subnet and one private subnet.
    
Subnets:
    Public Subnets: Associated with the internet gateway to allow direct internet access.
    Private Subnets: Isolated from the internet, used for internal resources.
    
Route Tables:
    Configured route tables for each subnet to direct traffic appropriately.
    Public subnets route traffic to the internet gateway.
    Private subnets route traffic to the NAT gateway.
Internet Gateway (IGW):
    Created three IGWs, one for each VPC, to provide internet access to public subnets.

NAT Gateway:
    Deployed a NAT gateway in each public subnet to allow private instances to access the internet.

Transit Gateway:
    Set up a transit gateway to enable communication between private subnets across VPCs.

EC2 Instances:
    Provisioned EC2 instances in each subnet (public and private).
    Hosted a dummy website on private instances.

###############################################################################################################
Testing and Verification:
Ping Operation:
    Successfully tested connectivity between EC2 instances using ping.

Curl Operation:
    Verified website availability by curling the dummy website hosted on private instances from other EC2 instances.

# How to create VPC, Subnet, Internet Gateway and NAT Gateway.
There are 2 methods of creating VPC, Subnet, Internet Gateway and NAT Gateway. The first way involves creating each service individually in their respective dashboards, and the other, involves creating all of them in one go.

We’ll be starting with the 1st method by creating all the services individually starting with the VPC.

## 1st Method

### VPC
Search for VPC on the search bar of the AWS console.
![1](https://github.com/user-attachments/assets/7921c92c-96bf-46ee-a746-a87d817146dc)

Click on ‘create vpc’
![2](https://github.com/user-attachments/assets/55fe2313-1dc3-44bf-b7d4-6b1ef2ba32bf)

Select VPC only, choose a name tag and input your starting IP
![3](https://github.com/user-attachments/assets/46453e3b-ff28-418c-9e2e-313aa6520f13)

Click on ‘create VPC’
![4](https://github.com/user-attachments/assets/9ce935f7-bcfd-484e-89a7-26a95ae7b274)
![5](https://github.com/user-attachments/assets/2b3819fb-cf62-4e33-8a63-462a88b58e5b)
 
### Subnet
Under the VPC dashboard, click on ‘Subnet’ and click ‘create subnet’
![6](https://github.com/user-attachments/assets/fd6d669e-3820-4a25-bdfb-1abeaf43afcf)

Select the VPC you just created
![7](https://github.com/user-attachments/assets/b33c4f6f-21bf-4d85-88dc-cff10df561fe)

Choose your subnet name, select availability zone and select your IP address range with this ip address: 10.0.0.0/24. (notice how we have 256 IPs available)
![8](https://github.com/user-attachments/assets/a59a7aae-71d2-4807-84f6-d065ace8c8e0)

Click on ‘create subnet’
![9](https://github.com/user-attachments/assets/873cb588-ef57-4d37-952c-33d9044d1fb4)
 
### Internet Gateway
Under the VPC dashboard, click on ‘Internet Gateway’ and click ‘create Internet Gateway’
![10](https://github.com/user-attachments/assets/51606c55-7410-4ecb-b73e-c6d924fcf9b8)

Choose a name for Internet Gateway and click ‘create’
![11](https://github.com/user-attachments/assets/95225012-5a17-46c3-8a2c-feec91adbb21)

Notice how the Internet Gateways State says ‘Detached’
![12](https://github.com/user-attachments/assets/ccf1b437-77a5-4627-8551-86ecc30a9eef)

To attach it to your VPC, click on ‘Actions’ and select ‘Attach to VPC’
![13](https://github.com/user-attachments/assets/cd4b50c7-cb1d-465e-a6f2-d1d7047da3c0)

Click on the search tab and select your VPC, then click ‘attach Internet Gateway’
![13 1](https://github.com/user-attachments/assets/49a42688-0f5a-457b-b515-99ad50f8254b)

The state is now shown attached.
![14](https://github.com/user-attachments/assets/17da745f-6666-4e09-a067-ea6bd9d25684)
 
### NAT Gateway
Under the VPC dashboard, click on ‘NAT Gateway’ and click ‘create NAT Gateway’
![15](https://github.com/user-attachments/assets/f3b80cb7-a7ca-4c92-9841-0a5b1a7f7a67)

Choose your NAT Gateway name, select your subnet, make your connectivity 'Public', Click on ‘Allocate Elastic IP’ and click on ‘Create NAT Gateway’
![16](https://github.com/user-attachments/assets/a2a0cf86-42b8-4973-934f-74f40c3224a4)
![17](https://github.com/user-attachments/assets/dc666824-e91f-40a2-bb62-55ecc0dcab88)
![18](https://github.com/user-attachments/assets/091912bb-bca6-4805-9656-c67628a52a76)


## 2nd Method

Search for VPC on the search bar of the AWS console.
![1](https://github.com/user-attachments/assets/7921c92c-96bf-46ee-a746-a87d817146dc)

Click on ‘Create VPC’
![2](https://github.com/user-attachments/assets/55fe2313-1dc3-44bf-b7d4-6b1ef2ba32bf)

Select VPC and more, choose a name tag and input your starting IP
![19](https://github.com/user-attachments/assets/db621653-59ce-47aa-a74b-6354ee074f23)

Under ‘number of availability zones’, select 2.
Under ‘number of public subnets’, select 2.
Under ‘number of private subnets’, select 4.
![20](https://github.com/user-attachments/assets/dfc47cd7-bff4-436a-9930-566badfae205)

Under NAT gateway, select ‘1 per AZ’.
Under endpoints, select S3 gateway.
Click on 'Create VPC’
![21](https://github.com/user-attachments/assets/3815f9e4-fa23-4cfd-8c35-d8e8bba7729a)
![22](https://github.com/user-attachments/assets/8ae71773-70fd-4d47-b394-72937b23ed0a)
![23](https://github.com/user-attachments/assets/441a1d37-9285-4481-abeb-af67873b1de4)

With this, you have created your VPC, Subnets, Internet gateway, and NAT gateway all on one go
![24](https://github.com/user-attachments/assets/a505e8ca-0b2d-449d-9b6a-f65a0d51c511)
![25](https://github.com/user-attachments/assets/7ddcf15d-8519-43c0-8b32-7a4c25fd3641)




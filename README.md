# with a single pod and using kops we can craete the containers
	create the ec2 instance in ubuntu in t2 medium.

	Change the server into root,update the server

	Install the docker and kubectl

chmod +x kubectl to excute and persmison

	move the kubectl file by using mv kubectl /usr/local/bin command
![Screenshot 2024-11-20 215405](https://github.com/user-attachments/assets/9e0d5c1c-cbc3-4c2e-8708-118b40eb8f3a)
	Installing the kops by using below command

curl -Lo kops https://github.com/kubernetes/kops/releases/download/$ (curl -s https://api.github.com/repos/kubernetes/kops/releases/latest | grep tag_name | cut -d '"' -f 4)/kops-linux-amd64
![Screenshot 2024-11-20 220321](https://github.com/user-attachments/assets/9ab57729-4239-4765-9f8e-100e8720d4f0)	
Execute the .bashrc by using source .bashrc command

vi .bashrc

![Screenshot 2024-11-20 221156](https://github.com/user-attachments/assets/9d245e48-6ddf-4f41-b322-43d6314e170c)
Create the IAM user and add the administrator policies to that user.

Configure the AWS CLI by using aws configure command.

Now give the access key and secret key and region and format in json.

![Screenshot 2024-11-20 223427](https://github.com/user-attachments/assets/3b182151-6d1d-4e63-a221-82ab0b4f9e3a)


![Screenshot 2024-11-21 001110](https://github.com/user-attachments/assets/4f984f5c-7ff0-4401-a0de-2633972a4d5f)



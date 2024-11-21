# with a single pod and using kops we can craete the containers  

# create the ec2 instance in ubuntu 

Change the server into root,update the server

Install the docker and kubectl

curl -LO "https://dl.k8s.io/release/$(curl -L -s https://dl.k8s.io/release/stable.txt)/bin/linux/amd64/kubectl"

chmod +x kubectl to excute and persmison

move the kubectl file by using mv kubectl /usr/local/bin command

kubectl version --client
![Screenshot 2024-11-20 215405](https://github.com/user-attachments/assets/9e0d5c1c-cbc3-4c2e-8708-118b40eb8f3a)
# now installing kops by using below command

curl -Lo kops https://github.com/kubernetes/kops/releases/download/$ (curl -s https://api.github.com/repos/kubernetes/kops/releases/latest | grep tag_name | cut -d '"' -f 4)/kops-linux-amd64
![Screenshot 2024-11-20 220321](https://github.com/user-attachments/assets/9ab57729-4239-4765-9f8e-100e8720d4f0)	
Execute the .bashrc by using source .bashrc command

vi .bashrc

given path here

export path=$path:/usr/bin/local

![Screenshot 2024-11-20 221156](https://github.com/user-attachments/assets/9d245e48-6ddf-4f41-b322-43d6314e170c)
Create the IAM user and add the administrator policies to that user.

Configure the AWS CLI by using aws configure command.

Now give the access key and secret key and region and format in json.

![Screenshot 2024-11-20 223427](https://github.com/user-attachments/assets/3b182151-6d1d-4e63-a221-82ab0b4f9e3a)
Create the s3 bucket 

aws s3api create-bucket --bucket bucketname --region us-east-1
![Screenshot 2024-11-20 234357](https://github.com/user-attachments/assets/d4bff695-a74b-440d-879d-2a63d92753c3)

Files inside the s3 bucket

Enable the s3 versioning

aws s3api put-bucket-versioning --bucket bucketname --versioning-configuration Status=Enabled

Export the s3 by using command
export kops_state_store=s3://kopsbucket

object also created in s3 buckek

![Screenshot 2024-11-21 001110](https://github.com/user-attachments/assets/4f984f5c-7ff0-4401-a0de-2633972a4d5f)
automatically ec2 instace created master nods and worker nodes
![Screenshot 2024-11-19 235930](https://github.com/user-attachments/assets/4e2d3526-5707-4414-98bf-0031fc6f94ba)
# creating yaml file inside the two pods cration

vi pod.yml

apiVersion: v1

kind: Pod

metadata:

  name: kops-pod
  
spec:

  containers:
  
    - name: gani70
    
      image: nginx
      
      ports:
      
      - containerPort: 80
      
    - name: gani70
    
      image: ubuntu
      
      command: ["sh", "-c", "while true; do echo 'welcome to skywaves'; sleep 10; done"]
      
:wq!

![Screenshot 2024-11-21 095130](https://github.com/user-attachments/assets/e069fa9d-6151-4527-94a8-34841738c87c)






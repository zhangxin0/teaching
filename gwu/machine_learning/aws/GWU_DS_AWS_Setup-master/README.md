# AWS Setup for GWU Data Science Students

This Repo contains setup information and screenshots for students to create an EC2 instance with Amazon's Deep Learning AMI on the GWU Data Science Program's account. It also contains information/setup instructions for configuring a secure Jupyter Notebook Server for both Mac/Windows machines.

---

## How to transfer files to/from an Amazon Web Services (AWS) EC2 instance from your machine.

---

1. Uploading a file **TO YOUR INSTANCE**

Open your computer terminal (**on your local machine**)  


```
scp -i "your_aws_key.pem" [file-name] [aws-instance-name]:~/[file-name]
```

Example

```
scp -i ~/Documents.aws.pem iris.csv ubuntu@ec2-52-207-225-47.compute-1.amazonaws.com:~/iris.csv
```

---

2. Downloading a file **FROM YOUR INSTANCE**  

Open your computer terminal (**on your local machine**)  
```
scp -i "your_aws_key.pem" [aws-instance-name]:~/ .
```

NOTE:->  .(dot) - Means current directory  

Example  

```
scp -i ~/Documents.aws.pem ubuntu@ec2-52-207-225-47.compute-1.amazonaws.com:~/iris.csv .
```

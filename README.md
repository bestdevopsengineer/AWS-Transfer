# AWS-Transfer = WS Transfer Family simplifies migration of SFTP, AS2, FTPS, and FTP based workflows to AWS.
Let say you have files on premise that you want to transfer into a s3 bucket in aws


## 1-create the s3 bucket


![Screenshot 2024-08-28 123935](https://github.com/user-attachments/assets/29dd0f78-7fb5-431c-8e57-bf9cb8fad073)


## 2-put a unique name 


![Screenshot 2024-08-28 123935](https://github.com/user-attachments/assets/91d699e0-b5f7-4e22-8b45-829177d67f76)


## 3-click on create bucket

![Screenshot 2024-08-28 123935](https://github.com/user-attachments/assets/dedd959d-d1d7-47bc-a13e-8310a5d90f84)


## 4- check your amazon s3 , you will see an S3 bucket created

![Screenshot 2024-08-28 123935](https://github.com/user-attachments/assets/15370684-6bab-408a-b35a-9df6d04232bc)



## 5- create a role that will give the right to aws transfer sever to manage the s3 bucket

![Screenshot 2024-08-28 123935](https://github.com/user-attachments/assets/15896ac5-5fbb-47a7-b2d4-501e48cfa494)


## 6-choose AWS service |  write the name of the service = "transfer" and click Next  


![Screenshot 2024-08-28 123935](https://github.com/user-attachments/assets/c723afad-75dc-4311-843a-010d11df9290)


## 7-Add the permission  ,I will git the aws transfer server the full access to my S3 bucket

![Screenshot 2024-08-28 123935](https://github.com/user-attachments/assets/1c052ca3-2953-461e-b0e3-476b54df335e)

## 8-add a role name and clcik create role

![Screenshot 2024-08-28 123935](https://github.com/user-attachments/assets/a041fd60-4ed3-42d8-875a-c7c313e7c052)


## 9-go to AWS TRANSFER fAMILY by writing transfer in the search bar

![Screenshot 2024-08-28 123935](https://github.com/user-attachments/assets/72ee4006-60f9-4cd1-b984-47083cdec947)


## 10-click on create server

![Screenshot 2024-08-28 123935](https://github.com/user-attachments/assets/c45867b4-3024-48fc-a3d9-38b6b27778de)

## 11-check SFTP for file transfer over secure shell if not check yet and click Next

![Screenshot 2024-08-28 123935](https://github.com/user-attachments/assets/83a28d72-12c2-4b39-a1d2-4cc947fbcb78)

## 12- choose service managed and click Next

## 13- choose publicly accessible and click Next

## 14-amazon S3 and click Next

## 15- click Next again  and create an server

## 16- As soon as the server is online, check it and click on add user and Next

![Screenshot 2024-08-28 123935](https://github.com/user-attachments/assets/74b6a703-de6e-4547-ae12-7082edc11a22)


## 17-add user name , choose the role you created from the beginning on step 8, choose your bucket you craeted at step 1

![Screenshot 2024-08-28 123935](https://github.com/user-attachments/assets/2c7af7d0-5ad3-40f6-9903-e20350dcf668)

## 18-go to the server you want to take files and transfer to S3 and create a ssh-key with ssh-keygen command , 
## create and copy the public key and paste at SSH PUBLIC KEYS

![Screenshot 2024-08-28 123935](https://github.com/user-attachments/assets/b202af9e-9227-4fcf-8a00-ba590e913ee9)

## 19- copy the public key and paste into ssh public key and click on Add

![Screenshot 2024-08-28 123935](https://github.com/user-attachments/assets/56fd962e-a1e3-40f6-9fc1-55eb37581be5)


## 20-Copy the endpoint and go to your server in the directory where you want to transfer files on cmd and 
## write sftp -i "path/to the/private-key-name" "username"@"endpoint"
## sftp -i mykeygen user@s-38550cb2cf3642bd9.server.transfer.us-east-2.amazonaws.com
![Screenshot 2024-08-28 123935](https://github.com/user-attachments/assets/6e6a128a-7bf8-4b9e-bf94-f34c2e6ce2fb)

## 21- to transfer a file name id_rsa to s3 
![Screenshot 2024-08-28 123935](https://github.com/user-attachments/assets/d4d25461-e3d4-4c17-825b-330320e515ff)

## 22- Go to your S3 bucket and you will see the file 


![Screenshot 2024-08-28 123935](https://github.com/user-attachments/assets/453f3bd5-8c80-41d3-90a0-acdc92f19deb)

you made it , let me know if you need help .. Now delete all the resource created so you wont get charged



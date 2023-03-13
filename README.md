# website-monitoring-and-recovery-with-python
Project: website monitoring &amp; recovery

## 1. Create server & run nginx container

### 1.1 Create server on Linode

![Capture d’écran 2023-03-13 à 19 22 05](https://user-images.githubusercontent.com/62488871/224831621-93f2d305-4f54-4d77-9414-75d9a072f0e9.png)

### 1.2 ssh into server and install docker

![Capture d’écran 2023-03-13 à 19 23 15](https://user-images.githubusercontent.com/62488871/224831852-bb19df18-f743-4cd5-a3bf-9db6736a6183.png)

![Capture d’écran 2023-03-13 à 19 33 36](https://user-images.githubusercontent.com/62488871/224831884-cb81aa3a-0c44-495e-bacf-b46a9f097711.png)

### 1.3 run nginx container on the server using docker & access the application from the browser

![Capture d’écran 2023-03-13 à 19 34 30](https://user-images.githubusercontent.com/62488871/224831938-b26a5ef3-6e66-4cb9-82a8-31f20771a411.png)

<img width="827" alt="Capture d’écran 2023-03-13 à 19 36 00" src="https://user-images.githubusercontent.com/62488871/224831970-0c2be7ee-c8d7-428d-875e-b46842499a01.png">

## 2. Write python code for email automation

### 2.1 Make request to application endpoint using requests module 

![Capture d’écran 2023-03-13 à 19 53 44](https://user-images.githubusercontent.com/62488871/224832015-9d0e218f-2e14-4cea-b2e7-719d1542e209.png)

### 2.2 Create a condition that checks the status code of the application

![Capture d’écran 2023-03-13 à 19 58 16](https://user-images.githubusercontent.com/62488871/224832067-e36eb292-e10a-4383-8482-2817e67d1c66.png)

### 2.3 If the status code is not successful, send an email notification to your gmail account using the smtplib library

![Capture d’écran 2023-03-13 à 20 34 48](https://user-images.githubusercontent.com/62488871/224832160-eb3144ef-c988-46c5-9dd6-7dfc85b549b5.png)

### 2.4 Set email credentials as environment variables as best security practice, access them via os module and set them inside editor

![Capture d’écran 2023-03-13 à 20 27 02](https://user-images.githubusercontent.com/62488871/224832205-0dada80e-09c6-4a70-aec3-b40bfacc32ef.png)

### 2.5 Test that email is sent for this condition

<img width="364" alt="Capture d’écran 2023-03-13 à 20 35 41" src="https://user-images.githubusercontent.com/62488871/224832225-ff1ea896-9c91-4c83-8d2a-7d4ebad8bd03.png">

### 2.6 Handle the case where there is a connection error using a try / except. Send an email if this exception is caught

![Capture d’écran 2023-03-13 à 20 43 54](https://user-images.githubusercontent.com/62488871/224832277-8cce6786-019d-4782-8beb-d0a524340072.png)

### 2.7 Test that email is sent for this condition

<img width="371" alt="Capture d’écran 2023-03-13 à 20 45 11" src="https://user-images.githubusercontent.com/62488871/224832337-c8a325b0-3473-4643-b241-1c4a0301065f.png">

### 2.8 Keep your code DRY. Use function that can be called in multiple places instead of repeating code

![Capture d’écran 2023-03-13 à 20 53 44](https://user-images.githubusercontent.com/62488871/224832390-f4f89a48-de22-4c9b-bf8f-be3f9d4198c3.png)

## 3. Write python code for recovery logic

### 3.1 Use paramiko library to connect to the server using ssh and restart the application

![Capture d’écran 2023-03-13 à 21 09 47](https://user-images.githubusercontent.com/62488871/224832470-81903d36-acd9-49fb-984b-70ab5bae4bc5.png)

### 3.2 Use linode_api4 library to connect to Linode and restart the server

![Capture d’écran 2023-03-13 à 21 22 20](https://user-images.githubusercontent.com/62488871/224832516-abecd421-b5b8-4ddc-ad5f-f3d0c034bf49.png)

![Capture d’écran 2023-03-13 à 21 22 58](https://user-images.githubusercontent.com/62488871/224832549-d26e54ae-d986-4121-bd59-65a3a2f3d1ec.png)

### 3.3 Waiting logic for server to restart before restarting the application, can use time module as extra waiting buffer

![Capture d’écran 2023-03-13 à 21 44 49](https://user-images.githubusercontent.com/62488871/224832574-24e664c5-5246-4436-a324-3801d4f79055.png)

## 4. Refactor code into small & reusable functions

![Capture d’écran 2023-03-13 à 21 47 45](https://user-images.githubusercontent.com/62488871/224832612-6593030b-30da-42ef-8625-288f3f5ea2d4.png)

## 5. Schedule task so it runs automatically using schedule module

![Capture d’écran 2023-03-13 à 21 52 38](https://user-images.githubusercontent.com/62488871/224832648-bd015bc7-a714-4a66-a1ea-6f265a0bb7cb.png)

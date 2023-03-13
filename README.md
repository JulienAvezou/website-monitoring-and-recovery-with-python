# website-monitoring-and-recovery-with-python
Project: website monitoring &amp; recovery

## 1. Create server & run nginx container

### 1.1 Create server on Linode

### 1.2 ssh into server and install docker

### 1.3 run nginx container on the server using docker & access the application from the browser

## 2. Write python code for email automation

### 2.1 Make request to application endpoint using requests module 

### 2.2 Create a condition that checks the status code of the application

### 2.3 If the status code is not successful, send an email notification to your gmail account using the smtplib library

### 2.4 Set email credentials as environment variables as best security practice, access them via os module and set them inside editor

### 2.5 Test that email is sent for this condition

### 2.6 Handle the case where there is a connection error using a try / except. Send an email if this exception is caught

### 2.7 Test that email is sent for this condition

### 2.8 Keep your code DRY. Use function that can be called in multiple places instead of repeating code

## 3. Write python code for recovery logic

### 3.1 Use paramiko library to connect to the server using ssh and restart the application

### 3.2 Use linode_api4 library to connect to Linode and restart the server

### 3.3 Waiting logic for server to restart before restarting the application, can use time module as extra waiting buffer

## 4. Refactor code into small & reusable functions

## 5. Schedule task so it runs automatically using schedule module















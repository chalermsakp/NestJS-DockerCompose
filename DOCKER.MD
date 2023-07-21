# How to install Docker Compose for NestJS

##### 1. Download DockerDesktop

* [DockerDesktop](https://www.docker.com/products/docker-desktop/)


* (Now restart the system and try again)

##### 2. Open PowerShell as administrator and (Enable Hyper-V with)
* > dism.exe /Online /Enable-Feature:Microsoft-Hyper-V /All

* (Now restart the system and try again)

##### 3. Install WSL updates on Windows 11

* Open Start on Windows 11.

* Search for Command Prompt, right-click the top result, and select the Run as administrator option.

* Type the following command to update the WSL on Windows 11 and press Enter : 
* > wsl --update

##### 4. Open Programs DorkerDesktop

* Sign in

##### 4. Create Dockerfile for Project

* Create Dockerfile
* Copy to Dockerfile

* ><br># ใช้ Version ของ Node.js
<br>FROM node:16<br>
<br># ตั้งค่าไดเรกทอรีทำงานภายในคอนเทนเนอร์
<br>WORKDIR /app<br>
<br># คัดลอกไฟล์ package.json และ package-lock.json ไปยังคอนเทนเนอร์
<br>COPY package*.json ./<br>
<br># ติดตั้ง dependencies ของแอปพลิเคชัน
<br>RUN npm install<br>
<br># คัดลอกโค้ดทั้งหมดของแอปพลิเคชันไปยังคอนเทนเนอร์
<br>COPY . .<br>
<br># เปิดพอร์ตที่แอปพลิเคชัน Nest.js ทำงานอยู่
<br>EXPOSE 3000<br>
<br># เริ่มต้นแอปพลิเคชัน Nest.js
<br>CMD ["npm", "run", "start:prod"]

##### 5. Create docker-compose.yml
* Create file docker-compose.yml
* Copy to docker-compose.yml

* >version: '3.9'
<br>services:
  <br>nestjs-app:
    <br># ใช้ context <br>ที่ชี้ไปที่ตำแหน่งของแอปพลิเคชัน Nest.js
    <br>build:
      <br>context: .
      <br>dockerfile: Dockerfile
    <br># กำหนดพอร์ตให้แอปพลิเคชันเรียกใช้งาน
    <br>ports:
      <br>- "3000:3000"

##### 6. Run Terminal
* >docker-compose up --build
# GitFlow Design

### master

* เป็น Branch สำหรับจัดการซอร์สโค้ดเพื่อ release ขึ้นไปที่ Production ให้กับ User
* ทำการติดเวอร์ชันแท็ก
* ในส่วนของ Branch นี้จะไม่ทำ Develop

### develop
* เป็น Branch ที่ดำเนินการพัฒนางานเป็นหลัก
* แก้ไข Bug
* พัฒนาโดยสร้าง Branch Feature ใหม่ขึ้นมา

##### 3. Install WSL updates on Windows 11

* Open Start on Windows 11.

* Search for Command Prompt, right-click the top result, and select the Run as administrator option.

* Type the following command to update the WSL on Windows 11 and press Enter : 
* > wsl --update

##### 4. Open Programs DorkerDesktop

* Sign in

##### 5. Create Dockerfile for Project

* Open Project NestJS
* Download Dockerfile
* [Download](https://github.com/jumpondbe8/nestjs-prototype/blob/feature/dockercompose-cs-174%2C176/Dockerfile)
* Add Dockerfile To Project

##### 6. Create docker-compose.yml
* Download file docker-compose.yml
* [Download](https://github.com/jumpondbe8/nestjs-prototype/blob/feature/dockercompose-cs-174%2C176/docker-compose.yml)
* Add docker-compose.yml To Project

##### 7. Run Terminal
* >docker-compose up --build
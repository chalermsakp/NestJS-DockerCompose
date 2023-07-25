# GitFlow Design

### Production

* เป็น Branch สำหรับจัดการซอร์สโค้ดเพื่อ release ขึ้นไปที่ Production ให้กับ User
* ทำการติดเวอร์ชันแท็ก
* ในส่วนของ Branch นี้จะไม่ทำ Develop
* CI Auto Deploy To Env. Production

### Develop
* เป็น Branch ที่ดำเนินการพัฒนางานเป็นหลัก
* แก้ไข Bug
* พัฒนาโดยสร้าง Branch Feature ใหม่ขึ้นมา
* CI Auto Deploy To Env. Dev


### Feature

* เป็น Branch ที่ถูกสร้างขึ้นจาก Branch develop
ทำการพัฒนา feature ใหม่
* ถ้างานที่พัฒนาเสร็จแล้ว จะทำการ Merge ไปที่ Branch develop
* [Feature Diagram](https://raw.githubusercontent.com/chalermsakp/NestJS-DockerCompose/05401591120f582422e0d4d5460eebbaec4420ad/Picture/Gitflow-Diagram/02%20Feature%20branches.svg)

### FixBug

* ถ้าเจอ Bug อยู่ในเวอร์ชันที่ Release ไปแล้ว จะทำการแตก Branch ออกมาจาก master และทำการแก้ไขโดยด่วน
* หลังจากที่ทำการแก้ไขแล้ว จะทำการ Merge ไปที่ Branch Production และ Branch Develop ทันที
* [Fixbug Diagram](https://github.com/chalermsakp/NestJS-DockerCompose/blob/main/Picture/Gitflow-Diagram/04%20Hotfix%20branches.svg)
### Release

* เป็น Branch ที่ถูกสร้างขึ้นจาก Branch Develop
* เป็น Branch ที่ใช้สำหรับดำเนินการ Test หรือปรับแต่งรายละเอียดให้สมบูรณ์ เช่น ทำการแก้ Bug หรือเพิ่ม Feature ก่อนที่จะ Release
* เมื่อทำการ QA เสร็จแล้ว จะทำการ Merge ไปที่ Branch Production และ Branch Develop
* [Release Diamgram](https://github.com/chalermsakp/NestJS-DockerCompose/blob/main/Picture/Gitflow-Diagram/03%20Release%20branches.svg)

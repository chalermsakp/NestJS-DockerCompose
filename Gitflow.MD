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


### FixBug

* ถ้าเจอบั๊กอยู่ในเวอร์ชันที่ release ไปแล้ว จะทำการแตก Branch ออกมาจาก master และทำการแก้ไขโดยด่วน
* หลังจากที่ทำการแก้ไขแล้ว จะทำการ Merge ไปที่ Branch Production และ Branch develop ทันที

### Release

* เป็น Branch ที่ถูกสร้างขึ้นจาก Branch develop
* เป็น Branch ที่ใช้สำหรับดำเนินการ Test หรือปรับแต่งรายละเอียดให้สมบูรณ์ เช่น ทำการแก้ Bug หรือเพิ่ม Feature ก่อนที่จะ Release
* เมื่อทำการ QA เสร็จแล้ว จะทำการ Merge ไปที่ Branch Production และ Branch develop

[GitFlow Diagarm](google.com)
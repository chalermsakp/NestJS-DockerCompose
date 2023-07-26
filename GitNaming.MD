# GitNaming Best Practices

### Tags Semantic Versioning 
* เป็นเครื่องมือที่ช่วยให้เราทำเครื่องหมายรุ่นในเวอร์ชันของโค้ดที่เราต้องการสร้างและเปิดใช้งานใน Production หรือสำหรับระบุจุดที่สำคัญในการพัฒนา
#### Major.Minor.Patch.
[Semantic Versioning Struceture](https://lh3.googleusercontent.com/W0hV4oisvCb5b0iTzbFCZSbXZiQXLwncMnBTRaE8RcaG3nv2stKPbfReK84Dry_-gfi9cOvdorPCaJWMXx1IZHm33plYzxQQi119nxHS0uv-dii0VEhB-t7nwPZ62DZGVm1U2Grh=s1600)
* > Example. 1.0.0 <br> major (เมเจอร์)= 1 <br>
minor (ไมเนอร์) = 0 <br>
patch (แพทช์) = 0 <br><br>
สำหรับการตั้งชื่อ Tag เป็นที่นิยมใช้รูปแบบเลขเวอร์ชัน ตัวอย่างเช่น v1.0.0, v2.1.3, v3.2.0 ซึ่งระบุถึงเลขเวอร์ชันของโค้ดที่เราต้องการ
* > Major => การเปลี่ยนแปลงซอร์ฟแวร์ที่เปลี่ยนไปเลย หรือ มีการเรียกใช้ function ในซอร์ฟแวร์ที่อาจจะไม่เหมือนเดิมเลย เช่น getFullName() คือการเรียกถึงข้อมูล ชื่อ-สกุล ของผู้ใช้งานในรุ่นก่อนหน้า แต่ในรุ่นใหม่ต้องเรียกใช้งานด้วย get_fullname()<br><br> Minor => การเปลี่ยนแปลง เล็ก ๆ น้อย ๆ โดยอาจจะเหมือนเดิมทุกอย่างแต่เพิ่ม function บางอย่างที่ทำให้การทำงานง่ายขึ้น เช่น ก่อนหน้านี้อาจจะต้องเรียกใช้ทั้งชื่อ-สกุล อาจจะเพิ่ม getFirstName() และ getLastName() เพิ่มเข้ามา
<br><br>Patch => การแก้ไขบัค ที่เกิดขึ้นจาก function เดิม ๆ

### GitNaming
* > May branch off: master
<br>Must merge back into: master and develop
<br>Tag: increment patch number
<br>Branch naming convention: hotfix-* or hotfix/*
* >Example.
<br>
=>feature/cs-174-xxx โดยที่ xxx คือชื่อของ Feature ที่กำลังพัฒนา
<br>=>release/x.x.x โดยที่ x.x.x คือเลขเวอร์ชันที่ตั้งของ Release
<br>=>hotfix/xxx โดยที่ xxx คือชื่อของ Bug ที่กำลังแก้ไข

#### Refer 
* https://leanpub.com/git-flow/read
* https://www.gitkraken.com/gitkon/semantic-versioning-git-tags
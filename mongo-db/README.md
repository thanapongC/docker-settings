วิธีการใช้งาน
1. สร้างไฟล์ docker-compose.yml
สร้างไฟล์ใหม่ชื่อ docker-compose.yml
คัดลอกโค้ดด้านบนลงในไฟล์
2. เริ่มต้น Jenkins
เรียกใช้คำสั่ง:

bash
คัดลอกโค้ด
docker-compose up -d
คำสั่งนี้จะดาวน์โหลดภาพ Jenkins และเริ่มต้นคอนเทนเนอร์

3. เข้าถึง Jenkins
เปิดเบราว์เซอร์และเข้า URL:

arduino
คัดลอกโค้ด
http://<IP-ADDRESS>:8080
ตัวอย่าง: http://localhost:8080 หรือ http://192.168.x.x:8080

4. ปลดล็อก Jenkins
เมื่อคุณเปิด Jenkins ครั้งแรก จะต้องใช้รหัสผ่านสำหรับการปลดล็อก
ค้นหารหัสผ่านได้จาก Log ของ Jenkins:
bash
คัดลอกโค้ด
docker logs jenkins
คุณจะพบข้อความลักษณะนี้:
css
คัดลอกโค้ด
Please use the following password to proceed to installation:
<your_initial_password>
ใช้รหัสผ่านที่ได้ไปปลดล็อกในหน้า Jenkins
5. ติดตั้งปลั๊กอินและตั้งค่า
หลังจากปลดล็อก คุณสามารถเลือกติดตั้งปลั๊กอินที่แนะนำหรือเลือกตามต้องการ
ตั้งค่าผู้ใช้งานและเริ่มต้นใช้งาน Jenkins
หมายเหตุ
Docker in Docker:

หากต้องการให้ Jenkins สามารถรัน Docker ได้ คุณต้องติดตั้ง Docker CLI และ Mount /var/run/docker.sock ไว้
ไฟล์ด้านบนตั้งค่าให้ Jenkins ใช้ Docker ได้โดยตรง
เพิ่มหน่วยความจำ:

Jenkins อาจต้องการหน่วยความจำเพิ่มเติม หากคุณพบปัญหา ให้แก้ไขในไฟล์ docker-compose.yml เช่น:
yaml
คัดลอกโค้ด
deploy:
  resources:
    limits:
      memory: 2g
สำรองข้อมูล:

ไฟล์และข้อมูลของ Jenkins จะถูกเก็บใน Volume ชื่อ jenkins_home หากต้องการสำรองข้อมูลให้ทำการ Backup Volume นี้

วิธีการใช้งาน:
สร้างไฟล์ docker-compose.yml:

สร้างไฟล์ใหม่ชื่อ docker-compose.yml
คัดลอกโค้ดด้านบนไปใส่ในไฟล์นี้
เริ่มต้นคอนเทนเนอร์:

bash
คัดลอกโค้ด
docker-compose up -d
ตรวจสอบสถานะ:

คุณสามารถตรวจสอบสถานะของคอนเทนเนอร์ได้ด้วยคำสั่ง:
bash
คัดลอกโค้ด
docker-compose ps
เข้าถึง Kong Gateway:

Proxy: http://localhost:8000
Admin API: http://localhost:8001
Dashboard (Konga): http://localhost:1337
หมายเหตุ:
หากต้องการตั้งค่าเพิ่มเติม เช่น การเปิดใช้งาน SSL หรือการปรับแต่งเพิ่มเติม คุณสามารถแก้ไขไฟล์ docker-compose.yml ตามความต้องการ
Kong Dashboard (Konga) เป็นส่วนเสริมสำหรับจัดการ Kong Gateway ผ่าน UI
คำอธิบาย
MySQL Container:

ใช้ MySQL เวอร์ชัน 8.0
กำหนด MYSQL_ROOT_PASSWORD สำหรับรหัสผ่าน root
สามารถกำหนดชื่อฐานข้อมูล (MYSQL_DATABASE), ผู้ใช้ (MYSQL_USER), และรหัสผ่านผู้ใช้ (MYSQL_PASSWORD)
phpMyAdmin Container:

ใช้ phpMyAdmin เพื่อจัดการ MySQL ผ่านอินเทอร์เฟซเว็บ
ผูกกับ MySQL container ผ่าน PMA_HOST และ PMA_PORT
ใช้รหัสผ่าน root เดียวกัน (MYSQL_ROOT_PASSWORD) เพื่อเข้าสู่ระบบ
Ports:

MySQL เปิดที่พอร์ต 3306 บนโฮสต์
phpMyAdmin เปิดที่พอร์ต 8080 บนโฮสต์ (เข้าผ่านเบราว์เซอร์ที่ http://localhost:8080)
Volumes:

mysql_data ใช้เก็บข้อมูลถาวรของ MySQL เพื่อไม่ให้หายเมื่อ container หยุด
Networks:

ทั้ง MySQL และ phpMyAdmin ใช้เครือข่ายเดียวกัน (mysql_network) เพื่อให้สื่อสารกันได้
การใช้งาน
บันทึกไฟล์นี้เป็น docker-compose.yml

รันคำสั่ง:

bash
คัดลอกโค้ด
docker-compose up -d
เข้า phpMyAdmin ผ่านเบราว์เซอร์ที่:

arduino
คัดลอกโค้ด
http://localhost:8080
ใช้ root และรหัสผ่านที่คุณตั้งใน MYSQL_ROOT_PASSWORD

เชื่อมต่อ MySQL ที่ localhost:3306 จากแอปพลิเคชันของคุณโดยใช้ค่าการตั้งค่าที่ระบุไว้ใน docker-compose.yml
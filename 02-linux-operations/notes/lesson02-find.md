Lesson 02 : find
find คืออะไร ?

find คือคำสั่งสำหรับค้นหาไฟล์และ Folder

ถ้า grep ใช้หา "ข้อความ"

find ใช้หา "ไฟล์"

ทำไม Data Engineer ต้องรู้ find

ลองนึกภาพว่า

พี่เข้ามารับงานต่อจากคนเก่า

เปิด Project แล้วเจอ

ETL Scripts
CSV Files
Log Files
Backup Files
Config Files

รวมกันหลายพันไฟล์

แล้วหัวหน้าถาม

customer.csv อยู่ไหน ?

คงไม่มีใครนั่งเปิดทีละ Folder

สิ่งที่ทำคือใช้ find ให้ระบบหาให้

Windows VS Linux

Windows

ใช้ Search Box

Linux

ใช้ find

แนวคิดเหมือนกัน

แค่ Linux ทำได้เร็วกว่าและยืดหยุ่นกว่า

ตัวอย่างง่ายที่สุด

หาไฟล์ชื่อ customer.csv

find . -name "customer.csv"

อ่านคำสั่งนี้ให้ออก

find

= ค้นหา

.

= เริ่มค้นหาจาก Folder ปัจจุบัน

-name

= ค้นหาตามชื่อ

customer.csv

= ชื่อไฟล์ที่ต้องการหา

แปลเป็นภาษาคน

find . -name "customer.csv"

หมายถึง

"ค้นหาไฟล์ชื่อ customer.csv จาก Folder ปัจจุบันลงไปทุก Folder"

ใช้จริงในงาน Data Engineer

หาไฟล์ CSV

find . -name "*.csv"

หาไฟล์ Log

find . -name "*.log"

หาไฟล์ SQL

find . -name "*.sql"

หาไฟล์ Backup

find . -name "*.bak"

ตัวอย่างในงานจริง

Business แจ้งว่า

customer_20260609.csv หายไป

สิ่งแรกที่ Data Engineer มักทำ

find . -name "customer_20260609.csv"

เพื่อดูว่า

อยู่ Folder ไหน
ถูกย้ายไปหรือยัง
ถูก Backup ไว้หรือไม่
Production Mindset

มือใหม่

เปิด Folder แล้วไล่หา

เปิดอีก Folder แล้วไล่หา

เปิดอีก Folder แล้วไล่หา

มืออาชีพ

find . -name "*.csv"

แล้วให้ระบบหาให้

grep VS find

grep

= หา "ข้อความ"

ตัวอย่าง

grep "ERROR" etl.log

find

= หา "ไฟล์"

ตัวอย่าง

find . -name "*.log"

สิ่งที่ต้องจำ

find = ค้นหาไฟล์และ Folder

คำสั่งที่ใช้บ่อย

find . -name "customer.csv"

find . -name "*.csv"

find . -name "*.log"

find . -name "*.sql"

สรุป

find เป็นคำสั่งสำหรับค้นหาไฟล์และ Folder

เป็นหนึ่งในคำสั่งที่ Data Engineer ใช้บ่อยมาก

โดยเฉพาะเวลาต้องหา

CSV Files
Log Files
SQL Scripts
Config Files
Backup Files

เมื่อ Project เริ่มใหญ่ขึ้น

find จะช่วยลดเวลาจากการไล่หาไฟล์ทีละ Folder เหลือเพียงไม่กี่วินาที
tail คืออะไร ?

tail คือคำสั่งสำหรับดูข้อมูลส่วนท้ายของไฟล์

ส่วนใหญ่ใช้กับ Log Files

เช่น

etl.log
scheduler.log
application.log
api.log
ทำไม Data Engineer ต้องรู้ tail

ลองนึกภาพว่า ETL กำลังรันอยู่

ไฟล์ Log มี 100,000 บรรทัด

เราไม่ได้อยากดูทั้งหมด

เราอยากรู้แค่ว่า

ตอนนี้เกิดอะไรขึ้นล่าสุด

tail จึงเป็นคำสั่งที่ช่วยดูข้อมูลล่าสุดของไฟล์ได้อย่างรวดเร็ว

Windows VS Linux

Windows

เปิด Notepad
เลื่อนลงล่าง
Refresh
เลื่อนลงล่างอีก

Linux

tail etl.log

ใช้ทำอะไรได้บ้าง
เช็คว่า Job จบหรือยัง
ดู Error ล่าสุด
ดู Progress ของ ETL
Monitor Log แบบ Real-Time
ตรวจสอบ Scheduler
ตัวอย่างการใช้งาน

ดู 10 บรรทัดสุดท้าย

tail etl.log

Option ที่ใช้บ่อย
-n

ใช้กำหนดจำนวนบรรทัดที่ต้องการดู

ดู 20 บรรทัดล่าสุด

tail -n 20 etl.log

ดู 50 บรรทัดล่าสุด

tail -n 50 etl.log

ดู 100 บรรทัดล่าสุด

tail -n 100 etl.log

-f

f = Follow

ใช้ดู Log แบบ Real-Time

tail -f etl.log

เมื่อ Log ถูกเขียนเพิ่ม

ข้อมูลจะเด้งขึ้นมาทันที

เหมือนดู Live สดของ Log

ออกจากโหมดนี้

Ctrl + C

-n + -f

ใช้ร่วมกันได้

tail -n 50 -f etl.log

ความหมาย

แสดง 50 บรรทัดล่าสุด
จากนั้นเฝ้าดู Log ต่อแบบ Real-Time

เป็นรูปแบบที่ใช้บ่อยมากใน Production

ตัวอย่างในงานจริง

Customer ETL กำลังรันตอนเที่ยงคืน

Data Engineer เปิด

tail -n 30 -f customer_etl.log

แล้วเฝ้าดู

Load Customer...

Load Product...

Load Branch...

Load Transaction...

ถ้ามี

ERROR : Connection Timeout

ก็รู้ทันทีว่าระบบพัง

grep VS find VS tail

grep

= หา "ข้อความ"

ตัวอย่าง

grep "ERROR" etl.log

find

= หา "ไฟล์"

ตัวอย่าง

find . -name "*.log"

tail

= ดู "ข้อมูลล่าสุด"

ตัวอย่าง

tail -f etl.log

Production Mindset

เวลาระบบมีปัญหา

ลำดับการใช้งานมักเป็น

หาไฟล์ Log

find . -name "*.log"

ดูข้อมูลล่าสุด

tail -n 50 etl.log

หา Error

grep "ERROR" etl.log

สิ่งที่ต้องจำ

tail

= ดูท้ายไฟล์

tail -n 50

= ดู 50 บรรทัดล่าสุด

tail -f

= ดู Log แบบ Real-Time

tail -n 50 -f

= ดู 50 บรรทัดล่าสุด + ดูต่อแบบ Real-Time

สรุป

tail เป็นคำสั่งสำหรับดูข้อมูลส่วนท้ายของไฟล์

เหมาะสำหรับการ Monitor ETL และตรวจสอบ Log ใน Production

คำสั่งที่ใช้บ่อยที่สุด

tail etl.log

tail -n 50 etl.log

tail -f etl.log

tail -n 50 -f etl.log

Checkpoint
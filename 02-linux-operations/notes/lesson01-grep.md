# Lesson 01 : grep

grep คือคำสั่งสำหรับค้นหาข้อความภายในไฟล์

ถ้า PowerShell มี Select-String

Linux ก็มี grep

---

## ทำไมต้องรู้ grep

ลองนึกภาพว่า ETL รันตอนตี 2

เช้ามา Business โทรมาบอกว่า

"พี่ครับ Job ล้ม"

ไฟล์ Log มีเป็นหมื่นบรรทัด

ไม่มีใครนั่งเลื่อนอ่านทีละบรรทัด

สิ่งแรกที่ Data Engineer ทำคือค้นหา Error ให้เจอก่อน

grep จึงเป็นหนึ่งในคำสั่งที่ถูกใช้บ่อยที่สุด

---

## Windows VS Linux

Windows

Select-String "ERROR" etl.log

Linux

grep "ERROR" etl.log

แนวคิดเหมือนกัน

แค่เปลี่ยนชื่อคำสั่ง

---

## ใช้หาอะไรได้บ้าง

* ERROR
* FAILED
* Timeout
* Exception
* Job Name
* Customer ID
* Transaction ID

---

## ตัวอย่างการใช้งาน

หา Error

grep "ERROR" etl.log

หา Failed

grep "FAILED" etl.log

หา Timeout

grep "Timeout" api.log

หา Exception

grep "Exception" application.log

---

## สิ่งที่มือใหม่มักพลาด

Linux แยกตัวเล็กตัวใหญ่

ERROR

ไม่เท่ากับ

Error

และไม่เท่ากับ

error

ถ้าไม่อยากสนใจเรื่องนี้

grep -i "error" etl.log

-i ย่อมาจาก Ignore Case

---

## ตัวอย่างในงานจริง

Business แจ้งว่า Customer ETL ไม่เข้า Data Warehouse

สิ่งแรกที่ Data Engineer มักทำ

grep "ERROR" customer_etl.log

ถ้ายังไม่เจอ

grep "FAILED" customer_etl.log

ถ้ายังไม่เจออีก

grep "Exception" customer_etl.log

เพื่อหาสาเหตุให้เร็วที่สุด

---

## Production Mindset

Log 100 บรรทัด อ่านเองได้

Log 100,000 บรรทัด ไม่มีใครอ่านเอง

ใช้เครื่องมือช่วยค้นหา

grep คือหนึ่งในอาวุธพื้นฐานที่สุดของคนดูแล Production

---

## สิ่งที่ต้องจำ

grep = ค้นหาข้อความในไฟล์

คำสั่งที่ใช้บ่อย

grep "ERROR" etl.log

grep "FAILED" etl.log

grep -i "error" etl.log

---

## สรุป

grep เป็นคำสั่งสำหรับค้นหาข้อความภายในไฟล์

ใช้บ่อยมากในการตรวจสอบ

* ETL Logs
* Scheduler Logs
* Application Logs
* API Logs

เมื่อเจอปัญหาใน Production

grep มักเป็นหนึ่งในคำสั่งแรกที่ถูกใช้เพื่อหาสาเหตุของปัญหา

---

## Checkpoint

ถ้าต้องการค้นหาคำว่า error โดยไม่สนตัวเล็กตัวใหญ่

จะใช้คำสั่งอะไร ?

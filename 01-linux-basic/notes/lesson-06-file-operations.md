# Lesson 06 : File Operations 📄

## 🎯 เป้าหมาย

เรียนรู้การ Copy, Move, Rename และ Delete ไฟล์ใน Linux

---

## 📌 cp

Copy File

ใช้คัดลอกไฟล์

ตัวอย่าง

cp booking.csv archive/

ผลลัพธ์

booking.csv ยังคงอยู่

และมี booking.csv เพิ่มใน archive

---

## 📌 mv

Move File

ใช้ย้ายไฟล์

ตัวอย่าง

mv customer.csv archive/

ผลลัพธ์

customer.csv ถูกย้ายไป archive

และหายจากตำแหน่งเดิม

---

## 📌 Rename File

Linux ใช้ mv ในการเปลี่ยนชื่อไฟล์

ตัวอย่าง

mv GL_BALANCE.csv GL_BALANCE_20260607.csv

ผลลัพธ์

GL_BALANCE.csv

กลายเป็น

GL_BALANCE_20260607.csv

---

## 📌 rm

Remove File

ใช้ลบไฟล์

ตัวอย่าง

rm customer.csv

ผลลัพธ์

customer.csv ถูกลบออก

---

## ⚠️ ข้อควรระวัง

rm เป็นการลบจริง

Command Line Linux ไม่มี Recycle Bin

ดังนั้นควรตรวจสอบชื่อไฟล์ก่อนลบทุกครั้ง

ตัวอย่าง

ls

หรือ

ls -l

ก่อนใช้ rm

---

## 🧠 จำง่ายๆ

cp

= Copy

ต้นฉบับยังอยู่

---

mv

= Move

ไฟล์หายจากที่เดิม

---

mv oldfile newfile

= Rename

---

rm

= Delete

ลบจริง

---

## 🔥 Cheat Sheet

| Command            | ความหมาย    |
| ------------------ | ----------- |
| cp file archive/   | Copy File   |
| mv file archive/   | Move File   |
| mv oldfile newfile | Rename File |
| rm file            | Delete File |

---

## 🎯 Summary

cp ใช้คัดลอกไฟล์

mv ใช้ย้ายไฟล์

mv สามารถใช้เปลี่ยนชื่อไฟล์ได้

rm ใช้ลบไฟล์

⚠️ rm ควรใช้อย่างระมัดระวัง เพราะการลบผ่าน Command Line ไม่มี Recycle Bin ให้กู้คืนได้ง่าย

คำสั่งเหล่านี้เป็นพื้นฐานสำคัญของ ETL และ Data Automation บน Linux

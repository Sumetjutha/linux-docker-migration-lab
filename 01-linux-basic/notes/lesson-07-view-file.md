# Lesson 07 : View File 📄

## 🎯 เป้าหมาย

เรียนรู้การเปิดดูข้อมูลภายในไฟล์บน Linux

---

## 📌 cat

ใช้แสดงข้อมูลภายในไฟล์

ตัวอย่าง

cat customer.csv

ผลลัพธ์

CustomerID,CustomerName
1001,John
1002,Mary

---

## 📌 เปรียบเทียบกับ Windows

PowerShell

Get-Content customer.csv

Linux

cat customer.csv

---

## 📌 ตัวอย่าง ETL

ตรวจสอบข้อมูลในไฟล์

cat booking.csv

---

## 📌 ตัวอย่าง Log

ตรวจสอบ Error

cat error.log

---

## 📌 ความแตกต่างระหว่าง ls และ cat

ls

= ดูว่า Folder นี้มีไฟล์อะไรบ้าง

---

cat

= ดูข้อมูลข้างในไฟล์

---

## ⚠️ ข้อควรระวัง

ถ้าไฟล์ใหญ่มาก

เช่น หลายแสนหรือหลายล้านบรรทัด

การใช้ cat อาจทำให้ข้อมูลไหลเต็มหน้าจอ

ในอนาคตจะมีคำสั่ง

head

tail

less

มาช่วยดูไฟล์ขนาดใหญ่

---

## 🧠 จำง่ายๆ

ls

= ดูรายชื่อไฟล์

cat

= ดูข้อมูลในไฟล์

---

## 🔥 Cheat Sheet

| Command          | ความหมาย          |
| ---------------- | ----------------- |
| ls               | ดูรายการไฟล์      |
| cat customer.csv | ดูข้อมูลในไฟล์    |
| cat error.log    | ดู Log หรือ Error |

---

## 🎯 Summary

cat ใช้เปิดดูข้อมูลภายในไฟล์

เหมือน Get-Content ใน PowerShell

เหมาะสำหรับตรวจสอบข้อมูล CSV, TXT และ Log File ในงาน ETL และ Data Automation

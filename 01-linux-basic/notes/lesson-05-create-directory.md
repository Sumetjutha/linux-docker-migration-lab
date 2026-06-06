# Lesson 05 : Create Directory 📁

## 🎯 เป้าหมาย

เรียนรู้การสร้าง Folder ใน Linux

---

## 📌 mkdir

Make Directory

ใช้สำหรับสร้าง Folder

ตัวอย่าง

mkdir backup

ผลลัพธ์

backup

---

## 📌 ตัวอย่าง ETL

สร้างโครงสร้าง Project

mkdir input

mkdir output

mkdir archive

mkdir log

ผลลัพธ์

/production

├── input

├── output

├── archive

└── log

---

## 📌 mkdir -p

ใช้สร้าง Folder หลายชั้นพร้อมกัน

ตัวอย่าง

mkdir -p log/daily

ผลลัพธ์

log

└── daily

---

## 📌 ข้อดีของ mkdir -p

ถ้า Folder ชั้นบนยังไม่มี

Linux จะสร้างให้ทั้งหมด

ตัวอย่าง

mkdir -p archive/2026/january

ผลลัพธ์

archive

└── 2026

└── january

---

## 🧠 จำง่ายๆ

mkdir backup

= สร้าง Folder เดียว

mkdir -p log/daily

= สร้าง Folder หลายชั้น

---

## 🔥 Cheat Sheet

| Command            | ความหมาย              |
| ------------------ | --------------------- |
| mkdir backup       | สร้าง Folder เดียว    |
| mkdir -p log/daily | สร้าง Folder หลายชั้น |

---

## 🎯 Summary

mkdir ใช้สร้าง Folder

mkdir ใช้สร้าง Folder เดี่ยว

mkdir -p ใช้สร้าง Folder หลายชั้นในคำสั่งเดียว

เหมาะกับการสร้างโครงสร้าง Project ETL และ Data Pipeline

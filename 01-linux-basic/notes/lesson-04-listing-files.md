# Lesson 04 : Listing Files 📂

## 🎯 เป้าหมาย

เรียนรู้การดูไฟล์และ Folder ใน Linux

---

## 📌 ls

List

ใช้ดูว่ามีอะไรอยู่ใน Folder ปัจจุบัน

ตัวอย่าง

ls

ผลลัพธ์

input
archive
log
output

---

## 📌 ls -l

List Long Format

ใช้ดูรายการไฟล์แบบละเอียด

ตัวอย่าง

ls -l

ผลลัพธ์ตัวอย่าง

-rw-r--r-- booking.csv
-rw-r--r-- customer.csv
-rw-r--r-- product.csv

หมายเหตุ

ตอนนี้ยังไม่ต้องสนใจ Permission

เราจะเรียนใน Module ถัดไป

---

## 📌 ls -a

List All

ใช้ดูไฟล์ทั้งหมด รวมถึงไฟล์ซ่อน

ตัวอย่าง

ls -a

ผลลัพธ์ตัวอย่าง

.
..
.git
.gitignore
.env
booking.csv

---

## 🧠 จำง่ายๆ

ls

= ดูรายการไฟล์และ Folder

ls -l

= ดูรายการแบบละเอียด

ls -a

= ดูรายการทั้งหมด รวมไฟล์ซ่อน

---

## 🔥 Cheat Sheet

| Command | ความหมาย                    |
| ------- | --------------------------- |
| ls      | ดูรายการไฟล์และ Folder      |
| ls -l   | ดูรายการแบบละเอียด          |
| ls -a   | ดูรายการทั้งหมด รวมไฟล์ซ่อน |

---

## 🎯 Summary

ls เป็นคำสั่งสำหรับดูข้อมูลภายใน Folder

ls ใช้ดูรายการทั่วไป

ls -l ใช้ดูรายละเอียดเพิ่มเติม

ls -a ใช้ดูไฟล์ทั้งหมด รวมถึงไฟล์ซ่อน เช่น

.git
.gitignore
.env

# Lesson 02 : Working Directory & Path

## 1. pwd

`pwd` ย่อมาจาก `Print Working Directory`

ใช้สำหรับดูว่า ตอนนี้เราอยู่ที่ตำแหน่งไหนใน Linux

ตัวอย่าง

```bash
pwd
```

ผลลัพธ์ตัวอย่าง

```text
/etl/input
```

แปลว่า ตอนนี้เรากำลังยืนอยู่ที่ `/etl/input`

---

## 2. Current Working Directory

Current Working Directory คือ ตำแหน่งปัจจุบันที่เรากำลังทำงานอยู่

ถ้าเราอยู่ที่

```text
/etl
```

Linux จะใช้ `/etl` เป็นจุดเริ่มต้นในการหาไฟล์แบบ Relative Path

---

## 3. Absolute Path

Absolute Path คือ Path แบบเต็ม

ต้องเริ่มจาก Root `/` เสมอ

ตัวอย่าง

```text
/etl/input/file1.csv
```

ข้อดีคือ ไม่ว่าเราจะยืนอยู่ตรงไหน ก็อ้างอิงไฟล์นี้ได้ชัดเจน

---

## 4. Relative Path

Relative Path คือ Path ที่อ้างอิงจากตำแหน่งปัจจุบัน

ตัวอย่าง

ถ้าเรายืนอยู่ที่

```text
/etl
```

และไฟล์อยู่ที่

```text
/etl/input/file1.csv
```

เราสามารถเขียนแบบ Relative Path ได้ว่า

```text
input/file1.csv
```

สังเกตว่า Relative Path จะไม่ขึ้นต้นด้วย `/`

---

## 5. ตัวอย่างเปรียบเทียบ

| สถานะ | Path |
|---|---|
| Current Working Directory | `/etl` |
| Absolute Path | `/etl/input/file1.csv` |
| Relative Path | `input/file1.csv` |

---

## Summary

- `pwd` ใช้ดูว่าเรายืนอยู่ตรงไหนใน Linux
- Current Working Directory คือจุดที่เรากำลังทำงานอยู่
- Absolute Path เริ่มจาก `/`
- Relative Path อ้างอิงจากตำแหน่งปัจจุบัน
- ถ้า Path ขึ้นต้นด้วย `/` แปลว่าเป็น Absolute Path
- ถ้า Path ไม่ขึ้นต้นด้วย `/` แปลว่าเป็น Relative Path
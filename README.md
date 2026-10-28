# Chicken Lotto — หน้าเปิดแอปบน GitHub Pages

หน้านี้ทำ 2 อย่าง: เป็น **ไอคอนบนหน้าจอโฮม** และ **จำการเข้าระบบ** ให้แอป
ตัวแอปจริงอยู่ใน Google Apps Script ทั้งหมด

## ติดตั้งครั้งเดียว

1. ใน Apps Script ไปที่ **Deploy → New deployment → Web app**
   - Execute as: **Me**
   - Who has access: **Anyone** (มีระบบ PIN กันคนนอกแล้ว)
   - คัดลอกลิงก์ที่ลงท้ายด้วย `/exec`
2. สร้าง repository ใหม่บน GitHub (Public) เช่น `chicken-lotto`
3. อัปโหลดไฟล์ทั้งหมดในโฟลเดอร์นี้: `index.html`, `manifest.webmanifest` และโฟลเดอร์ `icons`
4. แก้ `index.html` บรรทัดเดียว: `const APP_URL = '...'` ให้เป็นลิงก์ `/exec` จากข้อ 1
5. ไปที่ **Settings → Pages → Branch: main / (root) → Save**
   รอ 1–2 นาที จะได้ลิงก์ `https://ชื่อบัญชี.github.io/chicken-lotto/`

## เพิ่มไอคอนลงหน้าจอโฮม

- **iPhone (Safari):** เปิดลิงก์ → ปุ่มแชร์ → เพิ่มไปยังหน้าจอโฮม
- **Android (Chrome):** เปิดลิงก์ → ⋮ → ติดตั้งแอป / เพิ่มลงในหน้าจอหลัก

## อัปเดตแอปภายหลัง (ไม่ต้องแตะ GitHub)

แก้โค้ดใน Apps Script แล้วไปที่ **Deploy → Manage deployments → ✏️ Edit → Version: New version → Deploy**
ลิงก์ `/exec` จะยังเหมือนเดิม หน้า GitHub นี้จึงไม่ต้องแก้อีก

> อย่ากด "New deployment" ซ้ำ เพราะจะได้ลิงก์ใหม่ และต้องกลับมาแก้ `APP_URL`

# TechSpace — Tailwind CSS v4 CLI Setup

เว็บไซต์ TechSpace สร้างด้วย Tailwind CSS v4 แบบ CLI (Node.js)

---

## โครงสร้างโปรเจกต์

```
techspace-tailwind-cli/
├── src/
│   ├── input.css       ← ไฟล์ CSS ต้นฉบับ (มี @import "tailwindcss")
│   ├── index.html
│   ├── products.html
│   ├── blog.html
│   └── contact.html
├── dist/
│   └── output.css      ← ไฟล์ CSS ที่ Tailwind สร้างให้ (อย่าแก้ไขตรงนี้)
├── package.json
└── README.md
```

---

## วิธีติดตั้งและรัน

### ขั้นตอนที่ 1 — ติดตั้ง Node.js
ดาวน์โหลดจาก https://nodejs.org แล้วติดตั้ง

### ขั้นตอนที่ 2 — ติดตั้ง dependencies
เปิด Terminal ในโฟลเดอร์ `techspace-tailwind-cli` แล้วพิมพ์:

```bash
npm install
```

### ขั้นตอนที่ 3 — รัน Tailwind CLI (Watch Mode)
```bash
npm run watch
```

หรือใช้คำสั่งตรงๆ:
```bash
npx @tailwindcss/cli -i ./src/input.css -o ./dist/output.css --watch
```

> `--watch` หมายถึงระบบจะคอมไพล์ CSS ใหม่ทุกครั้งที่คุณบันทึกไฟล์ HTML

### ขั้นตอนที่ 4 — เปิดเว็บไซต์
เปิดไฟล์ `src/index.html` ในเบราว์เซอร์

---

## วิธีอัปโหลดขึ้น GitHub

```bash
git init
git add .
git commit -m "TechSpace: Tailwind CSS v4 CLI setup"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/techspace.git
git push -u origin main
```

---

## หมายเหตุสำคัญ

- ไฟล์ `dist/output.css` จะถูกสร้างโดยอัตโนมัติเมื่อรัน `npm run watch`
- ห้ามแก้ไข `dist/output.css` โดยตรง ให้แก้ที่ `src/input.css` แทน
- Tailwind v4 ใช้ `@import "tailwindcss"` แทน `@tailwind base/components/utilities`

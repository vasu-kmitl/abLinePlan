# abLinePlan — AutoSteer Field Designer

เครื่องมือออกแบบแนวขับ (AB line) และขอบเขตแปลง สำหรับระบบขับอัตโนมัติในงานเกษตร
A browser tool for planning autosteer AB lines and field boundaries.

**วสุ อุดมเพทายกุล** · ภาควิชาวิศวกรรมระบบชีวภาพและเกษตร คณะวิศวกรรมศาสตร์ สจล.
**Vasu Udompetaikul** · Department of Biosystems and Agricultural Engineering, School of Engineering, KMITL
<vasu.ud@kmitl.ac.th>

---

## ลิงก์ใช้งาน / URLs

หลัง publish แล้ว (แทน `USERNAME` ด้วยชื่อบัญชี GitHub ของคุณ):

| ลิงก์ | ได้อะไร |
|---|---|
| `https://USERNAME.github.io/abLinePlan/` | **เวอร์ชันล่าสุด** — ใช้ลิงก์นี้กับหน้างาน |
| `https://USERNAME.github.io/abLinePlan/v1_9/` | v1.9 (ลิงก์ตายตัว ไม่เปลี่ยนตามการอัปเดต) |
| `https://USERNAME.github.io/abLinePlan/v1_8/` | v1.8 (ไว้ย้อนกลับถ้าเวอร์ชันใหม่มีปัญหา) |
| `https://USERNAME.github.io/abLinePlan/versions.html` | รายการเวอร์ชันทั้งหมด |

## วิธี publish ครั้งแรก (~10 นาที)

1. สมัคร/เข้า <https://github.com> → กด **+** มุมขวาบน → **New repository**
2. ตั้ง **Repository name** = `abLinePlan` · เลือก **Public** · กด **Create repository**
   > ชื่อ repo คือส่วนท้ายของ URL ดังนั้นต้องเป็น `abLinePlan` เป๊ะ ๆ เพื่อให้ได้ `/abLinePlan`
3. ในหน้า repo กด **uploading an existing file** → ลากไฟล์และโฟลเดอร์ทั้งหมดในนี้เข้าไป
   (`index.html`, `versions.html`, `README.md`, `.nojekyll`, โฟลเดอร์ `v1_9/`, `v1_8/`)
   → กด **Commit changes**
4. **Settings** (แถบบนของ repo) → **Pages** (เมนูซ้าย) → หัวข้อ *Build and deployment*
   → **Source: Deploy from a branch** · **Branch: `main`** · โฟลเดอร์ `/ (root)` → **Save**
5. รอ 1–2 นาที แล้วรีเฟรชหน้า Pages จะเห็น URL ขึ้นมา — เปิดได้เลย

## เวลาออกเวอร์ชันใหม่ (เช่น v1.10)

1. สร้างโฟลเดอร์ `v1_10/` แล้ววางไฟล์ใหม่ชื่อ `index.html` ข้างใน
2. เอาไฟล์เดียวกันทับ `index.html` ที่ root (เพื่อให้ `/abLinePlan/` = ล่าสุด)
3. เพิ่มบรรทัดใหม่ใน `versions.html`

ไฟล์เก่าไม่ต้องแตะ — ลิงก์ `v1_x` เดิมยังใช้ได้ตลอด

## หมายเหตุ

- **ต้องเป็น https** — `navigator.share` (ปุ่ม export บนมือถือ/แท็บเล็ต) และ `navigator.clipboard`
  ทำงานเฉพาะ secure context · GitHub Pages ให้ https อัตโนมัติอยู่แล้ว
- **v1.9 ฝัง Leaflet ไว้ในไฟล์แล้ว** เปิดได้แม้เน็ตไม่ดี ขาดแค่ภาพแผนที่พื้นหลัง
  (รูปแปลง เส้น AB แถวปลูก ยังวาดครบ) · v1.8 ยังต้องโหลด Leaflet จาก CDN
- **แผนที่พื้นหลัง** ยังต้องใช้เน็ต: Esri World Imagery (ดาวเทียม) และ OpenStreetMap
- ทุกอย่างทำงานในเบราว์เซอร์ทั้งหมด — ไม่มีการส่งไฟล์แปลงขึ้นเซิร์ฟเวอร์ใด ๆ

## License

Leaflet 1.9.4 (BSD-2-Clause) ฝังอยู่ในไฟล์ — © Volodymyr Agafonkin, CloudMade

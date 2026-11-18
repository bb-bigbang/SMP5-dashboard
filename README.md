# SMP5 Progress Dashboard (เวอร์ชันเว็บ)

เว็บแบบ static เปิดได้ทันทีบน GitHub Pages ไม่ต้องมี server

## โครงสร้าง
- `index.html` – หน้า dashboard ทั้งหมด (10 แท็บ)
- `data/*.csv` – ข้อมูลที่ใช้วาดกราฟ (สำเนา ณ วันที่ระบุในแต่ละแท็บ)
- `.nojekyll` – ให้ GitHub Pages เสิร์ฟไฟล์ตรงๆ

## ขึ้น GitHub Pages ครั้งแรก
1. สร้าง repository ใหม่บน GitHub (เช่น `smp5-dashboard`)
2. อัปโหลดไฟล์ทั้งหมดในโฟลเดอร์นี้ขึ้นไปที่ root ของ repo (ลากทั้ง `index.html`, `.nojekyll` และโฟลเดอร์ `data`)
3. ไปที่ **Settings → Pages** → Source: **Deploy from a branch** → Branch: `main` / `/ (root)` → Save
4. รอ 1–2 นาที แล้วเปิด `https://<username>.github.io/<repo-name>/`

## อัปเดตรายสัปดาห์
แทนที่ไฟล์ใน `data/` (และ `index.html` ถ้ามีการเปลี่ยนหน้า) แล้ว commit — เว็บจะอัปเดตเองภายในไม่กี่นาที

## หมายเหตุ
- Repo สาธารณะ = ใครก็เปิดเว็บและดาวน์โหลดไฟล์ CSV ได้
- เวอร์ชันนี้ **ไม่รวม** แท็บ 8 (CMS Bill & Price – ราคาสัญญา) และแท็บ 10 (Client DB – ข้อมูล AMOGH ของลูกค้า)
- ต้องเปิดผ่านเว็บ (GitHub Pages หรือ local server) ถ้าดับเบิลคลิก `index.html` จากเครื่องตรงๆ กราฟจะไม่ขึ้นเพราะเบราว์เซอร์บล็อกการอ่านไฟล์ CSV

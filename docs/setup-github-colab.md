# คู่มือตั้งค่า GitHub + Google Colab (ทำก่อนคาบแรก ใช้เวลา ~20 นาที)

เป้าหมาย: เมื่อจบคู่มือนี้ คุณต้องเปิด notebook ของวิชาใน Colab ได้ และบันทึกงานกลับเข้า repo ของตัวเองได้

## เช็กลิสต์

- [ ] มีบัญชี GitHub (ใช้ชื่อผู้ใช้ที่เหมาะสมกับงานวิชาการ)
- [ ] สร้าง repo ของตนเองจาก template แล้ว (ชื่อ `geoai-<รหัสนักศึกษา>`, Private)
- [ ] เพิ่มอาจารย์เป็น Collaborator แล้ว
- [ ] เปิด Colab ด้วย Google Account และรันเซลล์ทดสอบได้
- [ ] เปิด notebook ของวิชาผ่านป้าย Open in Colab ได้ และ Save a copy in Drive แล้ว
- [ ] ดาวน์โหลด .ipynb แล้วอัปโหลดเข้า repo ของตนเองบน github.com สำเร็จ 1 ครั้ง

## ขั้นที่ 1 — สร้าง repo ของคุณจาก template

1. เปิดหน้า repo ของวิชา (ลิงก์ประกาศในห้องเรียน)
2. กดปุ่มเขียว **Use this template → Create a new repository**
3. Repository name: `geoai-<รหัสนักศึกษา>` · เลือก **Private** · กด Create
4. ไปที่ **Settings → Collaborators → Add people** แล้วเพิ่มชื่อ GitHub ของอาจารย์

## ขั้นที่ 2 — เปิด Colab ครั้งแรก

1. ไปที่ <https://colab.research.google.com> ล็อกอินด้วย Google Account
2. กด **New notebook** แล้วพิมพ์ในเซลล์แรก: `print("Hello GeoAI")` กด Shift+Enter
3. เมนู **Runtime → Change runtime type** ดูตัวเลือก CPU/GPU (แล็บสัปดาห์ 1 ใช้ CPU ได้ แต่ **T4 GPU จะเร็วกว่า** ในส่วน zero-shot)

## ขั้นที่ 3 — เปิด notebook ของวิชา

1. เปิดไฟล์ `README.md` ของ repo ที่อาจารย์แชร์ (หรือ repo ของคุณเอง) แล้วกดป้าย **Open in Colab** ของสัปดาห์ที่ต้องการ
2. **ทำทันที:** เมนู **File → Save a copy in Drive** แล้วทำงานในสำเนาของคุณ (notebook ต้นฉบับบันทึกกลับไม่ได้ และงานจะหายถ้าปิดหน้าต่าง)
3. ไม่ต้อง Authorize GitHub เพราะ notebook ของวิชาเป็น repo สาธารณะ

## ขั้นที่ 4 — ส่งงานเข้า repo ของตัวเอง (ทุกสัปดาห์)

Colab ไม่มีเมนู Save a copy in GitHub แล้ว ให้ส่งงานด้วยการดาวน์โหลดและอัปโหลดแทน

1. ใน Colab: **File → Download → Download .ipynb**
2. เปลี่ยนชื่อไฟล์เป็น `week01_lab_<รหัส>.ipynb` (เปลี่ยนเลขสัปดาห์ตามจริง)
3. เปิด repo `geoai-<รหัสนักศึกษา>` บน github.com ไปที่โฟลเดอร์ `week01/lab/` → **Add file → Upload files** แล้วลากไฟล์ใส่
4. Commit message: `week01: lab + prompt log` → เลือก **Commit directly to the main branch** → **Commit changes**
5. ตรวจว่าไฟล์ขึ้นใน repo ของคุณบน github.com

> เคล็ดลับ: ถ้าเน็ตหลุดระหว่างทำแล็บ ให้เปิดสำเนาใน Google Drive ของคุณ (**File → Save a copy in Drive** ที่ทำไว้ในขั้นที่ 3) งานยังอยู่

## ปัญหาที่พบบ่อย

| อาการ | แก้ไข |
|---|---|
| ป้าย Open in Colab เปิดไม่ได้ / ค้างที่ "waiting for authorization from GitHub" | กด Cancel แล้วเปิดลิงก์ป้ายจาก README ของ repo ต้นแบบ (สาธารณะ) ใหม่ ถ้ายังไม่ได้ให้แจ้งอาจารย์ |
| `ModuleNotFoundError` | รันเซลล์ติดตั้งไลบรารีที่ต้นไฟล์ใหม่ (หลัง Runtime รีสตาร์ทต้องติดตั้งใหม่) |
| Session หลุด/ข้อมูลหาย | Colab ลบไฟล์ใน `/content` เมื่อ session จบ — เก็บผลลัพธ์สำคัญไว้ใน Drive หรือ commit เข้า repo |
| ดาวน์โหลดข้อมูลช้า/ล้มเหลว | รอสักครู่แล้วรันเซลล์ใหม่ (STAC เป็นบริการสาธารณะ อาจช้าช่วงคนใช้เยอะ) ถ้ายังไม่ได้ให้แจ้งอาจารย์ |
| ใช้ GPU ไม่ได้ | โควตาฟรีหมด ให้ใช้ CPU แล้วลดจำนวนภาพที่ทดสอบ |

## กติกา commit

- commit บ่อย ข้อความสั้นและบอกสิ่งที่ทำ
- **ห้าม** commit รหัสผ่าน/โทเคน/API key เข้า repo
- ไฟล์ข้อมูลขนาดใหญ่ (> 50 MB) เก็บใน Drive แล้วใส่ลิงก์ใน README ของสัปดาห์นั้น

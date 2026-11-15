# สัปดาห์ที่ 1 — GeoAI คืออะไร + บทนำ Vibe Coding

**CLO:** CLO1 (หลักการ GeoAI, spatial dependence/heterogeneity), CLO2 (ใช้โมเดลสำเร็จรูป), CLO4 (Vibe Coding + Explain This) · **เวลา:** 5 ชม. (จันทร์ ทฤษฎี/TBL 2 ชม. + อังคาร แล็บ 3 ชม.)

## ตารางสอน (ภาคเรียนที่ 2/2569)

| วัน | เวลา | ห้อง | เนื้อหา |
|---|---|---|---|
| จันทร์ | 15:00–17:00 | SC6 SC6204 | ทฤษฎี / TBL |
| อังคาร | 08:30–11:30 | SC6 SC6601C | แล็บ Colab |

## ก่อนวันจันทร์ 15:00 (ทำให้ครบ)

1. ตั้งค่า GitHub + Colab ตาม [`docs/setup-github-colab.md`](../docs/setup-github-colab.md) ให้ผ่านเช็กลิสต์ (วันจันทร์มี Colab Ready Check ท้ายคาบ)
2. อ่าน [`preclass/preclass-pack.md`](preclass/preclass-pack.md) (~40 นาที) — เนื้อหาในข้อสอบ iRAT มาจากเอกสารนี้
3. อ่านกติกา [`docs/explain-this-rule.md`](../docs/explain-this-rule.md) และ [`docs/prompt-template.md`](../docs/prompt-template.md)

## วันจันทร์ 15:00–17:00 (ในห้อง SC6204)

| ช่วง | กิจกรรม | ไฟล์ |
|---|---|---|
| 15:00–15:48 | iRAT (รายบุคคล) → tRAT (ทีม) → อุทธรณ์ | [`tbl/irat-trat.md`](tbl/irat-trat.md) |
| 15:53–16:33 | จัดชั้นโจทย์ 8 ใบ: ไม่ใช้ AI / ML / DL | [`tbl/sorting-cards.md`](tbl/sorting-cards.md) |
| 16:33–16:52 | มินิเล็กเชอร์ · Exit ticket (มีคำทำนายคะแนน CLIP) · ชี้แจงงานข้ามคืน | [`worksheets/student-worksheet.md`](worksheets/student-worksheet.md) |
| 16:52–17:00 | **Colab Ready Check** — เปิด notebook จาก repo ตนเอง รันเซลล์ 0.2 และ Save a copy in GitHub | [`lab/week01_lab.ipynb`](lab/week01_lab.ipynb) |

## คืนวันจันทร์ — งานข้ามคืน (≈25 นาที)

ทำตามใบงาน **ส่วน D**: (1) **Site Scouting** ตรวจ 5 พิกัดบน Google Earth แล้วบันทึกว่า "คุณ" เห็นอะไร *ก่อนเห็นผลโมเดล* (2) ร่าง Prompt #1 ตามเทมเพลตวิชา (ยังไม่ต้องส่งให้ AI)

## วันอังคาร 08:30–11:30 (ในห้อง SC6601C — เริ่มตรงเวลา)

| ช่วง | กิจกรรม |
|---|---|
| 08:30–08:55 | Recap + อาจารย์สาธิตสดวงจร Vibe Coding และกฎ Explain This |
| 08:55–09:45 | ส่วน 0–2: เปิด notebook, ดึงภาพ Sentinel-2, Bug Hunt, **ล็อก `truth`** |
| 09:45–09:55 | พัก |
| 09:55–10:45 | ส่วน 3–4: CLIP zero-shot + ภารกิจ Prompt #2 |
| 10:45–11:30 | ส่วน 5–6: Verify on map, Prompt Log, commit เข้า GitHub |

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YOUR_GITHUB_USER/geoai-kku/blob/main/week01/lab/week01_lab.ipynb)

## สิ่งที่ต้องส่ง (ภายในวันที่ประกาศ)

- [ ] `week01/lab/week01_lab_<รหัส>.ipynb` (มี Explain This ครบ + `truth` ที่ล็อกก่อนรันโมเดล + Verify on map)
- [ ] `week01/prompt_log_week01.md` (ส่งออกจาก notebook)
- [ ] ใบงานทีม (ส่วน A–C) ที่กรอกแล้ว — ผู้รายงานของทีมส่ง 1 ชุด **ก่อนเลิกคาบวันจันทร์**
- [ ] ใบงานส่วน D (Site Scouting) — ใช้ในแล็บ ไม่ต้องส่งแยก

## ไฟล์ .docx สำหรับพิมพ์

โฟลเดอร์ [`docx/`](docx/) มีฉบับ Word (ฟอนต์ TH Sarabun New 16 pt) ของ iRAT/tRAT, การ์ดจัดชั้นโจทย์, ใบงาน และ Pre-class Pack สำหรับพิมพ์แจก — เนื้อหาเหมือนไฟล์ .md

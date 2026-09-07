# myself-skills

ชุดแนวทางการทำงานส่วนตัวสำหรับพัฒนาผลิตภัณฑ์ซอฟต์แวร์ ตั้งแต่การทำความเข้าใจโจทย์ ออกแบบข้อมูลและประสบการณ์ผู้ใช้ พิสูจน์แนวคิด พัฒนา ทดสอบ จนถึงจัดส่งและส่งต่องาน

## โครงสร้าง

- `templates/personal-instructions.md` — กฎพื้นฐานสั้น ๆ ที่เหมาะใช้กับทุกโปรเจกต์
- `skills/product-to-production/` — workflow หลักสำหรับงานตั้งแต่แนวคิดจนพร้อมส่ง
- `skills/security-sensitive-change/` — งานที่มี security เป็นสาระสำคัญ
- `skills/dependency-change/` — การเพิ่ม อัปเกรด หรือประเมิน dependency และเทคโนโลยีใหม่
- `skills/evidence-research/` — การวิจัยเชิงหลักฐาน ตั้งคำถาม ประเมินแหล่งข้อมูล สังเคราะห์ข้อขัดแย้ง และอ้างอิงอย่างตรวจสอบได้

รายละเอียดเฉพาะโปรเจกต์ เช่น architecture, business rules, package manager และคำสั่งตรวจสอบ ควรอยู่ใน `AGENTS.md` ของโปรเจกต์นั้น ไม่ควรนำมาใส่ใน personal Skills

## หลักการใช้งาน

Skills เหล่านี้เป็นกรอบตัดสินใจ ไม่ใช่ checklist ที่ต้องทำครบทุกข้อทุกครั้ง ให้ปรับความลึกตามขอบเขต ความเสี่ยง และสถานะปัจจุบันของงาน:

- งานใหม่ตั้งแต่ศูนย์หรือ feature ขนาดใหญ่ ใช้ `product-to-production`
- งาน prototype ใช้โหมด prototype และหยุดเมื่อพิสูจน์สมมติฐานสำเร็จ
- งาน productionization ให้เริ่มจากตรวจของเดิมและรักษาส่วนที่ดีอยู่แล้ว
- ใช้ security หรือ dependency Skill เมื่อเรื่องนั้นเป็นสาระสำคัญของงาน
- ใช้ `evidence-research` เมื่อต้องค้นคว้าหลายแหล่ง ประเมินคุณภาพหลักฐาน หรือจัดทำข้อสรุปที่ตรวจสอบย้อนกลับได้

## การติดตั้ง

คัดลอก skill directory ที่ต้องการไปยัง personal skills directory ของ Codex หรือใช้ตัวติดตั้ง Skill จาก GitHub path ของแต่ละ directory

หลังแก้ไข Skill ให้ตรวจรูปแบบด้วย `quick_validate.py` จาก Skill Creator และปรับคำสั่งจากผลการใช้งานจริง ไม่เพิ่มกฎถาวรจากเหตุการณ์ครั้งเดียว

หรือรันการตรวจทั้งหมดใน container โดยไม่ต้องติดตั้ง dependency บนเครื่อง:

```sh
docker compose run --rm skill-test
```

หากติดตั้ง Docker Compose แบบ standalone ให้ใช้ `docker-compose run --rm skill-test`

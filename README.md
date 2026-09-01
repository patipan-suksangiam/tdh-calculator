# 📊 Pipe Flow Calculation (Siamraj Pump System)

<div align="center" style="margin: 20px 0;">
  <a href="https://patipan-suksangiam.github.io/tdh-calculator/" target="_blank" style="background-color: #0d47a1; color: white; padding: 14px 28px; border-radius: 8px; text-decoration: none; font-size: 16px; font-weight: bold; display: inline-block; box-shadow: 0 4px 6px rgba(0,0,0,0.1);">
    🚀 คลิกเปิดโปรแกรมคำนวณ (เปิดในแท็บใหม่)
  </a>
  <p style="margin-top: 10px; color: #546e7a; font-size: 14px;">(หน้านี้คู่มือยังคงเปิดอยู่เพื่อให้อ่านควบคู่กันได้)</p>
</div>

Professional System Head and Pressure Drop Calculator developed for engineers and technical sales teams at **Siamraj Public Company Limited**.

---

## 🌟 Key Features (คุณสมบัติเด่นของโปรแกรม)

1. **Comprehensive Liquid Database (ฐานข้อมูลของไหลครบถ้วน):**
   - น้ำ (Water at various temperatures: 10°C - 100°C)
   - เชื้อเพลิง (Diesel, Gasoline, Biodiesel B100, Ethanol)
   - น้ำมันหล่อลื่น (Engine Oil SAE 10, 30, 40)
   - สารเคมี (Methanol, Sulfuric Acid 98%, Caustic Soda 50%)
   - รองรับการกรอกข้อมูลแบบ Custom / Manual ได้อิสระ

2. **Accurate Flow & Fluid Mechanics (คำนวณกลศาสตร์ของไหลอย่างแม่นยำ):**
   - **Laminar Flow ($Re < 2000$):** ใช้สูตร Darcy friction factor แม่นยำตามทฤษฎี ($f = 64 / Re$)
   - **Turbulent Flow ($Re \ge 2000$):** ใช้สมการ **Swamee-Jain equation** ซึ่งเป็น Explicit approximation ของ Colebrook-White equation สำหรับคำนวณสัมประสิทธิ์ความเสียดทาน ($f$) ในท่อได้อย่างรวดเร็วและแม่นยำ
   - รองรับหน่วยอัตราการไหลหลายรูปแบบ: $\text{m}^3/\text{h}$, $\text{L/min}$, และ $\text{US GPM}$

3. **Pipe & Fittings Pressure Drop (คำนวณความดันตกในท่อและอุปกรณ์):**
   - เลือกขนาดท่อมาตรฐาน ANSI Sch 40 (ตั้งแต่ 1/2" ถึง 24") หรือระบุ Inner Diameter (ID) เอง
   - ฐานข้อมูล Fittings มาตรฐาน (Elbows, Tees, Valves, Check Valves, Strainers, Entrance/Exit) พร้อมค่า $K$ factor
   - คำนวณความดันตกในอุปกรณ์เฉพาะตัว (Equipment $\Delta P$) และ Safety Margin (%)

4. **System Conditions & NPSHa Calculation (คำนวณ TDH และ NPSHa):**
   - คำนวณ Total Dynamic Head (TDH) ตามวิธีมาตรฐาน **Crane TP-410 Method**
   - คำนวณ Net Positive Suction Head Available (NPSHa) พร้อมตรวจสอบความปลอดภัย ($NPSHa \ge 1\text{m}$ ขึ้นไป)

5. **Professional Reporting & PDF Export (รายงานและพิมพ์ออก PDF):**
   - ระบบสะสมรายการหลายเคสลงในตารางรายงานสรุปโครงการเดียว (Multi-case Project Summary)
   - ส่วนหัวรายงานในนาม **"SIAMRAJ PUBLIC COMPANY LIMITED"** พร้อมฟังก์ชันพิมพ์ (Print / Save as PDF) แบบ Landscape อัตโนมัติ

---

## 🚀 How to Use (วิธีใช้งานโปรแกรม)

1. **เปิดใช้งานโปรแกรม:**
   - คลิกปุ่ม **"🚀 คลิกเปิดโปรแกรมคำนวณ"** ด้านบนเพื่อเปิดโปรแกรมในแท็บใหม่ โดยหน้าคู่มือนี้จะยังคงเปิดอยู่เพื่อให้อ่านคำแนะนำควบคู่กันได้
2. **กรอกข้อมูลและเลือกของไหล:**
   - กำหนด **Tag Number / Service** (เช่น P-101A)
   - เลือกของไหลจาก Dropdown หรือกรอก Density / Viscosity เอง
   - กำหนดอัตราการไหล (Flow Rate) และเลือกหน่วย
3. **กำหนดข้อมูลท่อและอุปกรณ์:**
   - เลือกขนาดท่อ ANSI Sch 40 หรือระบุ ID, ความยาวท่อ และวัสดุท่อ (Carbon Steel, Stainless Steel, PVC/HDPE, Galvanized Iron)
   - เพิ่ม Fittings ที่ใช้ในระบบ (เช่น 90° Elbow, Gate Valve, Check Valve) และระบุจำนวน (Qty)
4. **กำหนดสภาวะของระบบ (System Conditions):**
   - ระบุความดันฝั่งดูด ($P_1$) และฝั่งส่ง ($P_2$) รวมถึงระดับความสูง ($Z_1, Z_2$)
   - หากต้องการเช็คค่า NPSHa ให้ติ๊กเลือก **Calculate NPSHa** และกรอก Vapor Pressure ($V_p$)
5. **คำนวณและจัดทำรายงาน:**
   - คลิกปุ่ม **CALCULATE** เพื่อดูผลลัพธ์ทันที
   - หากต้องการรวบรวมเป็นรายงานโครงการ ให้คลิก **+ ADD TO REPORT** เพื่อบันทึกลงตารางสรุป
   - คลิก **🖨️ Print / Save as PDF** เพื่อพิมพ์รายงานอย่างเป็นทางการในนามบริษัท

---

## 📄 License & Author
- **Author:** Patipan Suksangiam (Engineering Department)
- **Company:** Siamraj Public Company Limited

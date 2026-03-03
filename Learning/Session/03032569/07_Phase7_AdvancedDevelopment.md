# Phase 7 – Advanced Development

## Learning Objectives
- ทำความเข้าใจ Liquidity & Manipulation เช่น Internal/External Liquidity และ Liquidity Sweep
- พัฒนาทักษะ Position Management รวมถึง Partial TP, Scaling In/Out และ Risk Stacking
- ผสานแนวคิดขั้นสูงเข้ากับแผนเดิมโดยไม่สูญเสียวินัยด้านโครงสร้างและความเสี่ยง

## Introduction
เมื่อระบบพื้นฐานนิ่งแล้ว การยกระดับต้องโฟกัสที่การอ่านความตั้งใจของสถาบันและการจัดการพอร์ตอย่างยืดหยุ่น Phase นี้ช่วยให้คุณตีความ Liquidity Trap ได้ดีขึ้นและใช้เทคนิค Position Management เพื่อเพิ่มประสิทธิภาพของ RR โดยไม่ทำลายวินัยเดิม

## Core Concepts
1. **Liquidity Sweep & Stop Hunt** – เป็นการที่ราคาเจาะเหนือ resistance หรือใต้ support เพื่อกิน stop ของ retail ก่อนกลับทิศ สถาบันใช้วิธีนี้เพื่อรวบรวมคำสั่งและเข้าตามทิศตรงข้าม จึงต้องมองหาวิกยาว/ปริมาณ spike รอบระดับสำคัญ โดยเฉพาะช่วง London/NY open หรือข่าวแรง ๆ[12]
2. **Step-by-step การเทรด Liquidity Sweep** – (1) มาร์กระดับ swing สำคัญ (2) รอให้ราคาสร้าง sweep และ rejection ที่แรง (3) รอแท่งยืนยัน เช่น engulfing/pin bar (4) เข้าไม้สวนทิศ (5) วาง SL เหนือ wick sweep และตั้ง TP ที่ฝั่ง liquidity ถัดไป โดยควรรักษา RR ≥ 1:2[12]
3. **Position Management Techniques** – Scaling-in (pyramiding) คือการเพิ่ม position เมื่อราคาเดินตามแผน เพื่อลดความเสี่ยงช่วงแรกและขยายกำไรเมื่อมีคอนเฟิร์ม ส่วน Scaling-out คือการทยอยปิดกำไรเพื่อล็อกผลและลดความกดดันในการหาจุดออกที่สมบูรณ์แบบ[13]
4. **Risk Stacking อย่างมีวินัย** – การเพิ่ม lot ต้องระบุจุดเพิ่มไว้ล่วงหน้า (เช่น แต่ละ HH/H L ที่ยืนยัน) และยังต้องคุม total exposure ให้อยู่ใน risk plan เดิม เพื่อป้องกันการ over-leverage หลังเจอสัญญาณสวย

## Practical Example
- ระบุโซน liquidity รอบ high/low รายวัน เมื่อราคากวาด high แล้วทิ้ง wick ยาวพร้อม volume spike ให้รอแท่ง engulf ลงคอนเฟิร์มก่อนเข้า sell
- วาง SL เหนือ wick sweep และตั้ง TP แรกที่ low ก่อนหน้า หากราคาวิ่งต่อสามารถ scale-out 50% เพื่อเก็บกำไร แล้วปล่อยส่วนที่เหลือไปถึง zone หลัก
- หากต้องการ scale-in เพิ่ม ให้กำหนดว่าต้องเกิด CHOCH ลงใน LTF พร้อมปริมาณสนับสนุน และเพิ่มขนาดเท่ากับล็อตแรกเท่านั้น

## Common Mistakes
- รีบเข้าเพราะคาดว่าจะเกิด sweep ทั้งที่ราคายังไม่ทะลุ/ไม่มี rejection ชัดเจน
- เพิ่ม position โดยไม่กำหนดจุดและขนาดล่วงหน้า จน exposure สูงเกินกรอบเสี่ยง
- ทยอยปิดกำไรในไม้ที่ยังขาดทุน ทำให้ลดโอกาสกลับมาเท่าทุน

## Advanced Insight (Optional)
การจับคู่ Liquidity Sweep กับ Order Block + Fair Value Gap บน HTF สามารถสร้าง “confirmation model” ที่ใช้คัดกรองจุดกลับตัวที่มีโอกาสสูงกว่า และช่วยให้การ scale-in มีเหตุผลตามโครงสร้าง ไม่ใช่ตามความรู้สึก[12]

## Summary
Phase 7 ขยายระบบจาก “เทรดตามโครงสร้าง” ไปสู่ “เข้าใจเจตนาสถาบันและบริหาร position อย่างยืดหยุ่น” เมื่ออ่าน Liquidity Sweep ได้และใช้ scaling อย่างมีวินัย คุณจะเพิ่ม RR และควบคุมความเสี่ยงได้พร้อมกัน

## References
- [12] EBC Financial Group – “Liquidity Sweep in Forex: How to Trade the Trap” https://www.ebc.com/forex/liquidity-sweep-in-forex-how-to-trade-the-trap
- [13] TitanFX – “The Scaling-In and Scaling-Out Forex Trading Strategy and How to Implement It” https://titanfx.com/news/the-scaling-in-and-scaling-out-forex-trading-strategy-and-how-to-implement-it

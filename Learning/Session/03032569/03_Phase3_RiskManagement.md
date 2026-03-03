# Phase 3 – Risk Management System

## Learning Objectives
- วาง Stop Loss ตามโครงสร้างจริงและปรับ Break Even ด้วยเหตุผล ไม่ใช่อารมณ์
- กำหนด Daily Rules (กำไร/ขาดทุนสูงสุด) เพื่อป้องกันการพังพอร์ตในวันเดียว
- ผสานวินัยการจัดการความเสี่ยงเข้ากับระบบจิตวิทยาและบันทึกผลได้จริง

## Introduction
Risk Management คือหัวใจของระบบเทรด ทุกไอเดียจะไร้ประโยชน์ถ้าไม่มีกรอบจำกัดความเสียหาย Phase นี้ช่วยให้การวาง SL/BE และกฎรายวันกลายเป็นนิสัยเชิงระบบ ไม่ใช่การตัดสินใจหน้างานที่แปรผันตามอารมณ์

## Core Concepts
1. **Stop Loss ตามโครงสร้าง** – เป้าหมายของ SL คือออกเมื่อ setup ถูกทำลาย ไม่ใช่เพียงรักษา ego การวาง SL ควรอิง swing สำคัญหรือระดับที่ทำให้ bias เปลี่ยน หากวางคงที่ (static) ต้องคำนึงว่าราคาอาจสไลด์ทะลุระดับที่ตั้งไว้และเติมเต็มที่ราคาถัดไป[4]
2. **Break Even Logic** – การเลื่อน SL ไป BE อย่างไร้เหตุผลคือการย้ายจุดตัดสินใจไปที่ระดับที่มีความหมายเฉพาะตัว ไม่ได้สะท้อนโครงสร้างตลาด ต้องมีหลักฐาน เช่น โครงสร้างใหม่ยืนยันหรือผ่าน Liquidity ก่อนจึงค่อยเลื่อน[5]
3. **Daily Loss / Win Limit** – ตั้งเปอร์เซ็นต์หรือจำนวนเงินสูงสุดที่ยอมขาดทุนต่อวัน เช่น 1–3% หรือเท่ากับกำไรเฉลี่ยต่อวันที่ทำได้ หากแตะ limit ให้หยุดทันที ลดโอกาสเกิด revenge trade และปกป้องผลงานรายเดือน[6]
4. **Adjustable Position Size** – เมื่อใกล้แตะ limit สามารถลด position size ลงครึ่งหนึ่งเพื่อลดแรงกดดันและยังรักษาโอกาสฟื้นกำไร[6]

## Practical Example
- เทรดเดอร์กำหนดความเสี่ยง 1% ต่อไม้ วาง SL ใต้ swing ล่าสุดของโครงสร้าง LTF
- หากราคาเคลื่อนผ่าน internal liquidity และสร้างโครงสร้างใหม่ตามแผน จึงค่อยเลื่อน SL ไป BE
- กำหนด Daily Loss Limit = 2% หากขาดทุนสองไม้ติดให้พักทันที และบันทึกสาเหตุใน Journal

## Common Mistakes
- ขยับ SL เข้าใกล้ราคาปัจจุบันเพื่อ “รู้สึกปลอดภัย” แล้วโดนกวาดก่อนถึงเป้า
- ปรับ BE เร็วทันทีที่กำไรเล็กน้อย ทำให้โดนปิดโดยไม่มีสัญญาณโครงสร้าง
- ไม่มี Daily Rules ทำให้วันเสีย ๆ กลายเป็นรูรั่วที่กินกำไรทั้งเดือน

## Advanced Insight (Optional)
สามารถเชื่อมกฎ risk management เข้ากับ position sizing ขั้นสูง เช่น การ scale in/out ตามจุดยืนยัน เพื่อให้ RR จริงสะท้อนความเสี่ยงที่ควบคุมได้ตลอดการเทรด

## Summary
Phase 3 ทำให้ทุกการเทรดมีกรอบรับความเสี่ยงที่ชัดเจน ตั้งแต่ SL, BE, จนถึง Daily Rules เมื่อวินัยเหล่านี้ถูกทำซ้ำ ระบบจะรอดจาก drawdown และพร้อมต่อยอดในขั้นสูง

## References
- [4] IG Academy – “The importance of using stop-loss orders in forex” https://www.ig.com/en-ch/learn-to-trade/ig-academy/the-basics-of-forex-trading/stop-loss-orders-in-forex
- [5] Daily Price Action – “The Best Time to Move Your Stop Loss to Breakeven” https://dailypriceaction.com/blog/the-best-time-move-stop-loss-breakeven/
- [6] Trade That Swing – “Setting a Maximum Daily Loss When Day Trading” https://tradethatswing.com/setting-a-daily-loss-limit-when-day-trading/

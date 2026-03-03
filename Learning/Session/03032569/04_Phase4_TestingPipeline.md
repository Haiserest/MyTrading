# Phase 4 – Backtest → Forward Test → Live Execution

## Learning Objectives
- สร้างกระบวนการ Backtest ที่ระบุสถิติหลัก เช่น Win Rate, RR, Max Drawdown และตีความได้ถูกต้อง
- วางขั้นตอน Forward Test ให้เหมือนจริงทั้งสภาพแวดล้อม กฎ และการจดบันทึก
- ปิดวงจรด้วย Live Trading ที่รักษาวินัยเดิมและใช้ข้อมูลย้อนปรับปรุงระบบ

## Introduction
วงจร Backtest → Forward Test → Live คือสะพานจากไอเดียสู่ระบบที่เชื่อถือได้ การเก็บข้อมูลเชิงสถิติโดยละเอียดช่วยให้รู้ความคาดหวังของระบบ ส่วน Forward Test ตรวจสอบว่าพฤติกรรมจริงและสภาพจิตใจรองรับได้หรือไม่ ก่อนนำไปใช้กับเงินจริง

## Core Concepts
1. **Backtesting Metrics** – หลังรัน backtest ต้องดู Expected Return, Profit Factor, Win Rate, Average RR, Sharpe Ratio, Max Drawdown เพื่อประเมินความคุ้มค่าและความเสี่ยงของระบบ[7]
2. **ข้อมูลที่ต้องเก็บ** – บันทึกผลลัพธ์ต่อไม้, ขนาดกำไร/ขาดทุน, ความยาว drawdown และ RR จริง เพื่อหาว่าข้อใดต้องปรับก่อนเดินหน้าต่อ
3. **Forward Testing Setup** – ตั้ง demo/paper account ให้เหมือนสภาพจริง (ทุน, leverage, instrument) ทำตามกฎเดียวกับ backtest และจด journal อย่างละเอียดทุกไม้[8]
4. **Psychological Evaluation** – แม้ไม่มีเงินจริง Forward Test ต้องตั้งใจเหมือนจริงเพื่อดูว่ามีความโน้มเอียง เช่น ถือขาดทุนยาวหรือรีบปิดกำไรหรือไม่[8]
5. **Iterative Refinement** – เมื่อพบส่วนที่ไม่สอดคล้อง เช่น SL กว้างเกินหรือ RR ไม่ตามเป้า ให้วนกลับไปปรับใน backtest แล้ว forward test ใหม่ก่อนขึ้น live

## Practical Example
1. นำกฎจาก Phase 2–3 มารัน backtest ย้อนหลังอย่างน้อย 100 ไม้บนคู่เงินหลัก
2. วิเคราะห์สถิติ หาก Max Drawdown สูงเกิน 10% ให้ทบทวนจุดเข้า/ออกหรือปรับ position size
3. เปิด demo account ด้วยทุนเท่าจริง ตั้ง daily rules และบันทึกทุกไม้พร้อม screenshot
4. หลังครบ 30–50 ไม้ เปรียบเทียบผลกับ backtest ถ้ามี discrepancy ให้หาสาเหตุ (เช่น ความหน่วงหรือ slippage)
5. เมื่อสถิติใกล้เคียงและวินัยนิ่ง ค่อยย้ายไปบัญชีเล็กจริง พร้อมรักษากฎเดิมทั้งหมด

## Common Mistakes
- Backtest โดยไม่บันทึกสถิติสำคัญ ทำให้ไม่รู้ว่าระบบจริง ๆ ควรคาดหวังผลอย่างไร
- เปลี่ยนกฎกลางคันระหว่าง forward test ทำให้ข้อมูลเปรียบเทียบใช้ไม่ได้
- รีบเข้า live ทั้งที่ยังไม่ทดสอบภายใต้ความกดดันจริง (journal, daily rules, ฯลฯ)

## Advanced Insight (Optional)
ใช้ equity curve generator ดูความน่าจะเป็นของจำนวน SL ติดต่อกัน แล้วเตรียมแผนรับมือ เช่น การลดไซส์ชั่วคราวเมื่อเข้า drawdown ที่คาดการณ์ไว้[8]

## Summary
Phase 4 สร้างความเชื่อมั่นผ่านข้อมูล: Backtest ให้ได้ตัวเลขครบ, Forward Test ให้เหมือนจริงที่สุด แล้วค่อยเข้าสู่ Live ด้วยวินัยเดิม กระบวนการวนซ้ำนี้ทำให้ระบบพัฒนาได้ต่อเนื่องและลดความเสี่ยงผิดพลาดครั้งใหญ่

## References
- [7] FTMO Academy – “How to Backtest Trading Strategies” https://academy.ftmo.com/lesson/how-to-backtest-trading-strategies/
- [8] FTMO Academy – “Forward Testing of Trading Strategies” https://academy.ftmo.com/lesson/forward-testing-of-trading-strategies/

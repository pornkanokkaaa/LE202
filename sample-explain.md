# อธิบายโปรแกรมการทดลอง
## การทดลองที่ 1 เรื่อง การเขียนโปรแกรมเพื่อรันบนไมโครคอนโทรเลอร์
- อุปกรณ์
  - ไมโครคอนโทรเลอร์
  - usb
  - คอมพิวเตอร์หรือ แลปท็อป
 - บอร์ด=esp01
   - โปรแกรมส่วนแรก set ความเร็ว
   - ส่วนลูปก็จะให้แสดงผลตัวแปลเคาท์เพิ่มขึ้นเรื่อยๆโดยให้หน่วงเวลาหนึ่งวินาที
- รันคำสั่งอัพโหลด pio run -t upload
- คำสั่งแสดงผล pio device monito 
## การทดลองที่ 2 เรื่อง การเขียนโปรแกรมค้นหาไวไฟ
- อุปกรณ์
  - ไมโครคอนโทรเลอร์
  - usb
  - คอมพิวเตอร์หรือ แลปท็อป
- บอร์ด=esp01
  - โปรแกรมส่วนแรก เซ็ตอัพไวไฟให้พร้อมทำงาน
  - ส่วนลูป เริ่มต้นค้นหาไวไฟและแสดงผลไวไฟรอบตัว
- รันคำสั่งอัพโหลด pio run -t upload ปุ่มอัพโหลดและรีเซ็ต
- คำสั่งแสดงผล pio device monito เพื่อค้นหาไวไฟ
## การทดลองที่ 3 เรื่อง การเขียนโปรแกรมเอ้าพุทสัญญาณดิจิทัล
- อุปกรณ์
  - ไมโครคอนโทรเลอร์
  - usb
  - คอมพิวเตอร์หรือ แลปท็อป
  - พอร์ต
- บอร์ด=esp01
  - โปรแกรมส่วนแรก ให้0เป็นพอร์ต out put
  - ส่วนวนลูปทุกครึ่งวินาที ถ้าเคาท์เป็นเลขคี่ให้on เป็นเลขคู่ให้ off
- รันคำสั่งอัพโหลด pio run -t upload
- คำสั่งแสดงผล pio device monito
## การทดลองที่ 4 เรื่อง การเขียนโปรแกรมอินพุทสัญญาณดิจิทัล
- อุปกรณ์
  - ไมโครคอนโทรเลอร์
  - usb
  - คอมพิวเตอร์หรือ แลปท็อป
  - พอร์ต
- บอร์ด=esp01
  - โปรแกรมส่วนแรก พอร์ต0 เป็นinput พอร์ต 2เป็นout put
  - ส่วนลูปแสดงค่าที่อ่านได้ถ้าเป็น1ให้lowไปที่หลอดสองหรือไฟดับ ถ้าเป็น0ก็highไปที่หลอดสองก็คือไฟติด
  - สัญญาณinputที่พอร์ต0ก็จะเป็นตัวควบคุมให้ไฟเปิดหรือปิด
- รันคำสั่งอัพโหลด pio run -t upload
- คำสั่งแสดงผล pio device monito
## การทดลองที่ 5 เรื่อง การเขียนโปรแกรมเชื่อมต่อไวไฟและเว็บเซอร์เวอร์
- อุปกรณ์
  - ไมโครคอนโทรเลอร์
  - usb
  - คอมพิวเตอร์หรือ แลปท็อป
- บอร์ด=esp01
  - สร้างเว็บเซอเวอร์ผ่านไวไฟ ต้องเชื่อมต่อกับไวไฟ
  - โปรแกรมส่วนแรก set up เป็นการเชื่อมต่อserverกับไวไฟที่ได้เลือกไว้และset up เว็บเซอเวอร์
  - ส่วนลูป จะแสดงผล
- รันคำสั่งอัพโหลด pio run -t upload
- คำสั่งแสดงผล pio device monito
## การทดลองที่ 6 เรื่อง การเขียนโปรแกรมสร้างไวไฟแอคเซสพอยต์ (Wifi AP)
- อุปกรณ์
  - ไมโครคอนโทรเลอร์
  - usb
  - คอมพิวเตอร์หรือ แลปท็อป
  - โทรศัพท์
- บอร์ด=esp01
  - ต้องกำหนดชื่อและรหัสผ่าน ip address gateway subnet
  - หลังจากนั้นเตรียมเว็บเซอเวอร์ไว้และสร้าง แอคเซ็ปพ้อยท์กำหนดssidและpassword 
  - เมื่อเสร็จแล้วจะสร้างแอคเซ็ปพ้อยท์ขึ้นมาโดยไม่จำเป็นต้องใช้ที่อื่น
  
- รันคำสั่งอัพโหลด pio run -t upload
- คำสั่งแสดงผล pio device monito
- ทดลองเชื่อมกับโทรศัพท์เพื่อทดสอบ










# EmulsiV
## Program counter
![1](https://user-images.githubusercontent.com/98943979/160837407-35385d10-05c6-4746-832c-0570de1e743f.png)
ในขั้นตอนการปฏิบัติการทำงานจะมีการทำทีละคำสั่ง เมื่อเสร็จแล้วก็จะทำคำสั่งถัดไป  Program counter จะเป็นขั้นตอนการเปลี่ยนเป็นคำสั่งต่อไป โดยการ +4  byte เนื่องจาก 1 word หรือ่ 1 จะประกอบไปด้วย 4  byte
## Bus
![13](https://user-images.githubusercontent.com/98943979/160891057-2614b903-b787-4455-8dcd-818c469ef472.png)
เป็นการแปลง คำสั่ง Address ให้เป็น Data byte โดยเรียงจากหลังไปหน้า
## Intruction reg.
![14](https://user-images.githubusercontent.com/98943979/160883389-29c1a033-f7fd-4257-840a-be9838db7f1f.png)
เป็นการแปลง คำสั่ง เพื่อปฏิบัติใน ALU
# คำสั่ง
 ![15](https://user-images.githubusercontent.com/98943979/160891170-81fed520-37fe-4b97-9324-42a84b513b47.png)
- คำสั่งแรกคือ การนำ x0 + 32(ฐาน10)หรือ 20(ฐาน16) ใส่ในช่อง x1 
![16](https://user-images.githubusercontent.com/98943979/160887820-811425cd-db52-4050-8393-e738980bd4b5.png)
- คือการเอาแค่20 bit ของ Data byte ของคำสั่งใส่ลงไปใน x2 ( 1 word คือ 32 bit )
![18](https://user-images.githubusercontent.com/98943979/160888721-ff6a93e8-b971-4157-ac27-407d9380e090.png)
- นำค่า x1 มาแปลงเป็น Data byte แล้วใส่ใน x3 แต่ใส่แค่ 1 byte
![19](https://user-images.githubusercontent.com/98943979/160961339-a5e734f7-a13d-4328-8112-d1d25ba0d123.png)

- เมื่อ x3 = x0  จะบวก 16 (ฐาน10)หรือ 10 (ฐาน16) 
![20](https://user-images.githubusercontent.com/98943979/160958910-6d212790-f436-4ddb-90b9-29e370dead0c.png)
- เมื่อ x3 ไม่เท่ากับ x0 จะ run คำสั่งต่อไป
![21](https://user-images.githubusercontent.com/98943979/160959238-c0523d26-e142-4f3b-8a0a-2e7f0e089111.png)
- คำสั่งนี้เมื่อ x3 ไม่เท่ากับ x0 แปลงคำสั่งเป็น Data byte และใส่ใน x2 หรือก็คือ output แสดงผล
![22](https://user-images.githubusercontent.com/98943979/160959667-f74a8962-7831-4524-97f1-4a913d93cfc8.jpeg)
- นำ x1+1 แล้วใส่ใน x1 
![23](https://user-images.githubusercontent.com/98943979/160959694-c2e7f448-9070-48e3-93ea-e550ce99f2cf.jpeg)
- jal เป็นคำสั่ง jump คำสั่งนี้คือการ -16(ฐาน10)หรือ 10 (ฐาน16) จากคำสั่งที่แล้ว x1+1 และคำสั่งนี้เป็นการ black ไป -16(ฐาน10)หรือ 10 (ฐาน16) เมื่อทำสั่งสั่งวนลูปมาใหม่จะทำให้ output แสดงผลค่าถัดไป
เรื่อยๆ เนื่องจากเรานำ x1+1 ในคำสั่งก่อนหน้า

![24](https://user-images.githubusercontent.com/98943979/160961011-6c35400b-7365-4040-aef5-a07f7559a049.jpeg)
- เมื่อทำไปเรื่อยๆจนเป็น 00 จะไม่มี output แสดงผล เป็นการจบการทำงาน จะไม่มีoutput แสดงผลเพิ่ม

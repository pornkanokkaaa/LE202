# EmulsiV
## Program counter
![1](https://user-images.githubusercontent.com/98943979/160837407-35385d10-05c6-4746-832c-0570de1e743f.png)
ในขั้นตอนการปฏิบัติการทำงานจะมีการทำทีละคำสั่ง เมื่อเสร็จแล้วก็จะทำคำสั่งถัดไป  Program counter จะเป็นขั้นตอนการเปลี่ยนเป็นคำสั่งต่อไป โดยการ +4  byte เนื่องจาก 1 word หรือ่ 1 จะประกอบไปด้วย 4  byte
## Bus
![13](https://user-images.githubusercontent.com/98943979/160882548-4b1e5862-8927-4f92-88bc-b4e34ad9b9ea.png)
เป็นการแปลง คำสั่ง Address ให้เป็น Data byte โดยเรียงจากหลังไปหน้า
## Intruction reg.
![14](https://user-images.githubusercontent.com/98943979/160883389-29c1a033-f7fd-4257-840a-be9838db7f1f.png)
เป็นการแปลง คำสั่ง เพื่อปฏิบัติใน ALU
# คำสั่ง
![15](https://user-images.githubusercontent.com/98943979/160887104-aaf7694d-3db1-4671-9cca-3213c4e7f153.png)
-คำสั่งแรกคือ การนำ x0 + 32(ฐาน10)หรือ 20(ฐาน16) ใส่ในช่อง x1 
![16](https://user-images.githubusercontent.com/98943979/160887820-811425cd-db52-4050-8393-e738980bd4b5.png)
-คือการเอาแค่20 bit ของ Data byte ของคำสั่งใส่ลงไปใน x2 ( 1 word คือ 32 bit )
![18](https://user-images.githubusercontent.com/98943979/160888721-ff6a93e8-b971-4157-ac27-407d9380e090.png)
-นำค่า x1 มาแปลงเป็น Data byte แล้วใส่ใน x3 แต่ใส่แค่ 1 byte
![19](https://user-images.githubusercontent.com/98943979/160890284-647828d4-8c10-401d-8008-28e121d84135.png)

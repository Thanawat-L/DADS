DADS5001 AS03

By ธนวัฒน์ เหลืองวิโรจน์ 6610422005

ชุดข้อมูลนี้ประกอบด้วย "clinical features" หรือ "visual characteristics" ของผู้ป่วยที่ตรวจพบว่าเป็นมะเร็ง

แหล่งข้อมูล : [https://www.kaggle.com/datasets/sumanthnimmagadda/student-spending-dataset](https://www.kaggle.com/datasets/erdemtaha/cancer-data)

ตัวอย่าง Code : [https://github.com/Pomaccel/DADS5001-Data-Analytics-and-Data-Science-Tools-and-Programming/blob/main/6610422013_AS03.ipynb](https://github.com/Thanawat-L/DADS/blob/cad4ac9a063d1c7da8f29470c5ef05991ce014d4/DADS5001_Tools_6610422005_as03.ipynb)

อธิบายชุดข้อมูล
ชุดข้อมูลนี้ประกอบด้วย "clinical features" หรือ "visual characteristics" ของผู้ป่วยที่ตรวจพบว่าเป็นมะเร็ง

คุณสมบัติหลักของชุดข้อมูลคือดังนี้:
- diagnosis: ค่าที่บ่งบอกถึงการวินิจฉัยของมะเร็ง สามารถเป็น "M" (Malignant) หรือ "B" (Benign) ตามลำดับ
- radius_mean: ค่าเฉลี่ยของรัศมีของเซลล์มะเร็ง
- texture_mean: ค่าเฉลี่ยของความเรียบของเนื้อเยื่อ
- perimeter_mean: ค่าเฉลี่ยของเส้นรอบวงของเซลล์มะเร็ง
- area_mean: ค่าเฉลี่ยของพื้นที่ในส่วนของเซลล์มะเร็ง
- smoothness_mean: ค่าเฉลี่ยของความนุ่ม
- compactness_mean: ค่าเฉลี่ยของความหนาแน่น
- concavity_mean: ค่าเฉลี่ยของความเป็นโคน
- concave points_mean: ค่าเฉลี่ยของจุดแตกของโคน
- symmetry_mean: ค่าเฉลี่ยของความสมมาตร
- fractal_dimension_mean: ค่าเฉลี่ยของมิติเฟรกทัล
- และ parameter อื่นๆที่ตรวจวัด

เลือกกราฟ สำหรับการวิเคราะห์ข้อมูล

![newplot](https://github.com/Thanawat-L/DADS/assets/158482818/fad83f6a-3380-4f22-9552-c78cd4c17821)

เลือกใช้ Heatmap correlation plot เพราะต้องการทำความเข้าใจความสัมพันธ์ระหว่างคู่ของตัวแปรในชุดข้อมูล (มันดูง่ายกว่าอ่านจาก Table correlation ตรงๆ) 
โดยใช้ correlation coefficient ระหว่างตัวแปรทั้งหมดในรูปแบบของตารางที่มีสีแตกต่างกันตามค่า correlation coefficient ระหว่างคู่ของตัวแปร โดยที่ค่า correlation coefficient มีค่าตั้งแต่ -1 ถึง 1:

ค่า correlation coefficient เป็นบวกแสดงถึงความสัมพันธ์บวก (positive correlation) ระหว่างคู่ของตัวแปร หมายความว่าเมื่อค่าของตัวแปรหนึ่งเพิ่มขึ้น ค่าของตัวแปรอีกตัวจะเพิ่มขึ้นด้วย

ค่า correlation coefficient เป็นลบแสดงถึงความสัมพันธ์ลบ (negative correlation) ระหว่างคู่ของตัวแปร หมายความว่าเมื่อค่าของตัวแปรหนึ่งเพิ่มขึ้น ค่าของตัวแปรอีกตัวจะลดลง

ค่า correlation coefficient เป็นศูนย์แสดงถึงความสัมพันธ์ที่ไม่มี (หรือมีความสัมพันธ์ไม่ชัดเจน) ระหว่างคู่ของตัวแปร

ครั้งแรกตั้งใจจะใช้ทำ Feature selection ตัด feature ที่ไม่จำเป็นออก แต่ก็... ค่าใกล้ๆกันหมดเลย ก็เลยเอาไป fit model ทั้งหมดเลยครับ

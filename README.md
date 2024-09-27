# ROS2 Project Retake

**requirement**
- สร้างเต่า 1 ตัว(iron) ที่หน้าจอ 1
- สร้างเต่า 4 ตัว (Foxy,Noetic,Humble,Iron) ที่หน้าจอ 2 โดยมีจุดกำเนิดที่มุมซ้ายล่างของหน้าจอ
- สร้างเต่าที่สามารถควบคุมจากคีย์บอร์ด และทิ้งพิซซ่า โดยต้องสามารถเก็บเส้นทาง 4 ครั้ง และสามารถกดลบ และส่งค่ไป yaml file ได้
- เต่าสามารถ clear pizza ที่ยังไม่ได้กด save ได้
- เต่าทั้ง 4 ตัว ทิ้งพิซซ่าตามเต่าตัวแรกที่เดินเก็บ path 4 รอบไว้ โดยมี namespace ตามที่กำหนด
- เมื่อทิ้งพิซซ่าเรียบร้อยแล้ว ให้เต่าทั้ง 4 ตัวไปรวมกันอยู่ที่มุมบนขวาของหน้าจอ

**install**
- เริ่มจากโหลดไฟล์ 6525_6555.zip ลงเครื่อง<br>
- กด Extract here <br>
- สร้าง workspace <br>
```
mkdir -p ~/retake_ws/src
```
- เอา folder src ที่อยู่ใน folder 6525_6555 มาวางไว้ใน workspace <br>
- ทำการ build <br>
```
cd retake_ws
```
```
colcon build
```
```
cd
```
```
gedit .bashrc
```
- เพิ่มคำสั่งนี้ลงด้านล่างของไฟล์
```
source ~/retake_ws/install/setup.bash 
```

- หากยังไม่มี package turtlesim_plus ให้ลงตามนี้
```
cd retake_ws/src/
```
```
git clone https://github.com/tchoopojcharoen/turtlesim_plus.git
```
```
cd
```
```
colcon build
```

**launch** <br>
ในการ run file ให้สามารถใช้งานได้ ต้องพิมพ์คำสั่งดังนี้
```
ros2 launch exam1 launch.py 
```
```
ros2 run exam1 teleop_key.py 
```
![image](https://github.com/user-attachments/assets/2c8a9d95-8937-492f-94f9-6ea03031f04b)

ลอง spawn pizza จะมี info แสดงปุ่มที่กด เเละเมื่อวางพิซซ่า ก็จะบอกตำเเหน่ง เเละ จำนวนพิซซ่าที่เหลือ
![image](https://github.com/user-attachments/assets/ae7e0d2d-2207-42df-9914-6e89ad018cc3)

เมื่อกด o ก็จะ ทำการ clear pizza ที่ไม่ได้ save
![image](https://github.com/user-attachments/assets/2e2a7605-47e6-40d6-baea-3c1b72124221)

spawn pizza เเล้วทำการกด p เพื่อ save ครั้ง 1 
![image](https://github.com/user-attachments/assets/8bc5ba6d-9fbc-4850-b0ea-292915419051)

spawn pizza เเล้วทำการกด p เพื่อ save ครั้งที่ 2
![image](https://github.com/user-attachments/assets/b05a7b12-9262-47b9-b957-767c17524d0e)

spawn pizza เเล้วทำการกด p เพื่อ save 3
![image](https://github.com/user-attachments/assets/c19bda89-7679-4ab8-bcc1-81effde3703b)

spawn pizza ครั้งที่ 4
![image](https://github.com/user-attachments/assets/d3e9861d-287d-4f6d-9a9f-67a3f6fda7a2)

จากนั้นกด save คร้ังที่ 4 เต่าทั้ง 4 ตัวในหน้าต่าง copy_window จะทำการ spawn pizza ตามเส้นทางที่เต่าตัวแรกสร้างไว้
![image](https://github.com/user-attachments/assets/66329e62-f5c1-4cd8-b4d6-60730529de5e)

หลังจาก เต่า copy ออกมาวาดพิซซ่าตามครบเเล้ว เมื่อทุกตัวทำเสร็จ ก็จะไปรวมกันที่มุมขวาบน
![image](https://github.com/user-attachments/assets/7b2765a7-e847-480a-b2f3-20d28e9d6901)

finish >.<


**แก้ param in rqt_grqph**
สามารถแก้ param 
```
rqt
```

เปลี่ยน เพิ่ม จำนวน limit pizza บน rqt
![image](https://github.com/user-attachments/assets/7e1ed2a0-9134-4274-9155-2395b250bc3f)

check ค่า param บนเทอมินอล
![image](https://github.com/user-attachments/assets/de9809ac-dc2d-4d67-9571-72337ad9c113)

ลองเปลี่ยนค่า Kp_d Kp_theta
![image](https://github.com/user-attachments/assets/ec5b99ce-c457-4842-a125-0167f62aaf20)


# **Contributor** 
นายทัศน์พล สินเมือง 65340500025 <br>
นางสาวสิริมณี มณีเวศย์วโรดม 65340500055

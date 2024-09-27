# ROS2 Turtlesim Promax Project Reatake
**requirement**
- สร้างเต่าที่สามารถควบคุมจากคีย์บอร์ด และทิ้งพิซซ่า โดยต้องสามารถเก็บเส้นทาง 4 ครั้ง และสามารถกดลบ และส่งค่ไป yaml file ได้
- สร้างเต่าสำหรับ clear พิซซ่า ตามที่เต่าตัวแรกทิ้งไว้
- สร้างเต่า 4 ตัวในอีกหน้าจอหนึ่ง โดยเมีจุดกำเนิดที่มุมซ้ายล่างของหน้าจอ
- เต่าทั้ง 4 ตัว ทิ้งพิซซ่าตามเต่าตัวแรกที่เดินเก็บ path 4 รอบไว้ โดยมี namespace ตามที่กำหนด
- เมื่อทิ้งพิซซ่าเรียบร้อยแล้ว ให้เต่าทั้ง 4 ตัวไปรวมกันอยู่ที่มุมบนขวาของหน้าจอ

1.เริ่มจากโหลดไฟล์ 6525_6555.zip ลงเครื่อง<br>
2.กด Extract here<br>
3. สร้าง workspace <br>
```
mkdir -p ~/retake_ws/src
```
4.เอา folder src ที่อยู่ใน folder 6525_6555 มาวางไว้ใน workspace <br>
5.ทำการ build <br>
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
เพิ่ม source ~/retake_ws/install/setup.bash ลงด้านล่างของไฟล์

6.หากยังไม่มี package turtlesim_plus ให้ลงตามนี้
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
https://media.discordapp.net/attachments/1278701906335629323/1289068946380685324/image.png?ex=66f77a82&is=66f62902&hm=212ed143facc6881b985df0757de31de35da6ba47274f6383c18620fb97403d0&=&format=webp&quality=lossless&width=1110&height=660

**แก้ param in rqt_grqph**
สามารถแก้ param 
```
rqt
```
แก้ param แล้วกด enter
![image](https://github.com/user-attachments/assets/01db6e8d-3078-480a-8e61-b08c15167e4e)

**Demo**

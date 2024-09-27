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
4.เอา folder 6525_6555 มาวางไว้ใน workspace<br>
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
6.ลง pkg turtlesim_plus
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

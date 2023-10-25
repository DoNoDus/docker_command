===== Docker command ====

docker ps 
- แสดง container ที่กำลัง run อยู่

docker ps -a 
- แสดง  container ทั้งหมด

docker run -d -p [HOST PORT:CONTAINER PORT] --name [NAME IMAGE IF YOU WANT TO CONFIG] [IMAGE NAME]
- -p คือตัวที่จะบอกว่ารันที่ port อะไร
    -d คือการ run ใน daemon mode
  -name ใช้สำหรับการตั้งชื่อ container

docker rm [CONTAINER ID] 
- rm เป็นคำสั่งสำหรับลบ container 
  	(สามารถลบหลายอันในครั้งเดียวได้ เอา CONTAINER ID ใส่พร้อมกันไปเลย)

docker stop [CONTAINER ID OR ID] 
docker strat [CONTAINER ID OR ID] 
docker restrat [CONTAINER ID OR ID] 
docker logs [CONTAINER NAME OR ID]
-logs แสดงการทำงานทั้งหมด

docker images 
- images เป็นคำสั่งแสดง list ของ images ทั้งหมดที่มี

docker pull [IMAGE NAME]
- pull เป็นการสร้าง IMAGE โดยที่ไม่สร้าง CONTAINER (ดึงมาเฉยๆ บ่มีอิหยังดอก)

docker tag [IMAGE ID] [IMAGE NAME]
- tag เป็นอะไรไม่รู้ 5555 

docker push [IMAGE NAME]
- push เป็นเหมือนการอัพโค้ดลง git

docker save -o [FILE NAME] [NAME IMAGE]
- save เป็นการบันทึก IMAGE
- -o เป็นการคำสั่งสำหรับ Output

docker load -i [FILE NAME]
- load เป็นการนำเข้า IMAGE แบบไฟล์สำหรับคนที่ขี้เกียจดึงมาจาก repository

docker commit [CONTAINER ID] [IMAGE NAME T0 CREATE]
- commit เหมือนเป็นการทำให้ container เป็น image




เจาะลึก docker run
Interactive or Daemon [-it,-d]


docker inspect --format='{{.NetworkSettings.IPAddress}}' [DOCKER CONTAINER NAME]
docker inspect --format='{{.NetworkSettings.Ports}}' [DOCKER CONTAINER NAME]
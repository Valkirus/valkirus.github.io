---
layout: project
type: project
image: img/vacay/vacay-square.png
title: "Hexapod Robot"
date: 2023
published: true
labels:
  - Robot
  - 3D Design
summary: "A 6 legged robot intended for learning inverse kinematics and forward kinematics and cycling through them to make a hexapod move."
---

<img class="img-fluid" src="../img/vacay/vacay-home-page.png">

Hexapod เป็นหุ่นยนต์ 6 ขา ที่ผมทำการศึกษาการเคลื่อนที่ของพวกแมลงและออกแบบระแบบการเคลื่อนที่ที่ สามารถแปลงไปเป็น code แล้วนำมาคำนวนและขยับไปในทิศทางที่ต้องการ

ในการประดิษฐ์ ผมใช้ชิ้นส่วนที่ออกแบบ 3 มิติและนำมาปริ้นบนเครื่องปริ้น 3 มิติ ตัวหุ่นยนต์มีตัวคำนวน คือโทรศัพท์เพราะว่าเครื่องมันเล็กและมี sensor หลายอย่างครบในเครื่องเดียวแทนที่ว่าจะต่ออุปกรณ์กันเยอะ และตัวคุค กลไก (servo กับ touch sensor) เป็น servo2040 ใช้ chip [RP2040](https://github.com/pimoroni/pimoroni-pico) โดยเขียน firmware บนภาษา C ให้คุยกับ โทรศัพท์ผ่านระแบบ VCP CDC [VCP via USB-C](https://community.st.com/t5/stm32-mcus-embedded-software/stm32-vcp-by-usbc-cable-to-android-app/td-p/196371) 

ในโครงงานนี้ผมได้เรียนรู้ระแบบ inverse kinematics และ forward kinematics อย่างละเอียด รวมถึงการประยุคไปใช้ในภาษา C, การส่งข้อมูลผ่าน USB VCP และ การใช้โปรแกรม [Plasticity](https://www.plasticity.xyz/#features) ในการออกแบบชิ้นส่วนหุ่นยนต์

ตัวอย่าง code ที่ใช้ในการหาค่าที่ต้องขยับใน Gait:

{% gist b38240ffc44cff5c0992d4bf42c0289b1a344c91 %}
 
Source: <a href="https://github.com/theVacay/vacay">theVacay/vacay</a>

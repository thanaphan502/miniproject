### MINIPROJECT iot วัดอุณหภูมิและความชื้น สมาร์ทฟาร์ม
![minipro](https://user-images.githubusercontent.com/30243550/29305620-da1608ba-81c3-11e7-8fa7-b807d8ed304f.jpg)

### 1.การต่อวงจรและอุปกรณ์ที่ใช้
 #### **อุปกรณ์**
 1.สายจั้ม
 
 2.เซนเซอร์วัดอุณหภูมิและความชื้น DHT22
 
 3.จอ LCD
 
 4.Arduino NodeMCU ESP8266
 
 #### **การต่อวงจร**
 ต่อ DHT22 เข้ากับ Node MCU
 * ขา VCC -> Vin 3V NodeMCU
 * ขา Digital -> ขา D3 NodeMCU
 * ขา NULL -> NULL NodeMCU
 * ขา GND -> ขา G NodeMCU
 
 ต่อ NodeMCU กับ LCD แบบ LiquidCrystal_I2C lcd(0x3F, 16, 2);
 * ขา GND lcd -> ขา GND ของ NodeMCU
 * ขา VCC -> ขา Vin 5v NodeMCU
 * ขา SDA -> ขา D2 ของ NodeMCU
 * ขา SCL -> ขา D1 ของ NodeMCU
 
 ### 2.การสมัคร Domain Name และการทำ SSL (SHA256)
 #### สมัคร Domin Name 
 * เข้าไปที่ www.namecheap.com ทำการสมัครสมาชิก กรอกรายละเอียด
 * ทำการตั้งชื่อ Domain Name ที่ต้องการ และผูกบัตรเครดิต ทำการชำระเงิน 
 
 ![name](https://user-images.githubusercontent.com/30243550/29308372-e34ee008-81cf-11e7-822f-0fa28c5b289d.jpg)
 
 * จากนั้นไปที่ Account -> Domain list จากนั้นกด manage ที่โดเมน -> Advanced DNS ที่ A record ป้อน IP SERVER ของเรา 
 และ URL Reqiur ใส่ http:// ตามด้วยโดเมน
 
 #### ส่วนของ SERVER 
 * ไปที่ cloud.google.com ทำการ log in เข้าไปที่ server 
 * ติดตั้ง SSL Certificate โดยใช้คำสั่ง ดังต่อไปนี้
 
*********************************************************************************************

$ sudo apt-get update

$ sudo apt-get install software-properties-common

$ sudo add-apt-repository ppa:certbot/certbot

$ sudo apt-get update

$ sudo apt-get install python-certbot-apache 

$ sudo certbot --apache

$ sudo certbot --apache certonly

$ sudo certbot renew --dry-run

*จะต้องมี Domain Name เท่านั้นจึงจะทำได้ หากไม่มีจะไม่สามารถทำ SHA ได้



*********************************************************************************************
 
 
 
 
 


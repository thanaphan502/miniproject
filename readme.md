### MINIPROJECT iot วัดอุณหภูมิและความชื้น สมาร์ทฟาร์ม
![minipro](https://user-images.githubusercontent.com/30243550/29305620-da1608ba-81c3-11e7-8fa7-b807d8ed304f.jpg)

### 1.การต่อวงจรและอุปกรณ์ที่ใช้
 # **อุปกรณ์**
 1.สายจั้ม
 2.เซนเซอร์วัดอุณหภูมิและความชื้น DHT22
 3.จอ LCD
 4.Arduino NodeMCU ESP8266
 
 # **การต่อวงจร**
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
 
 


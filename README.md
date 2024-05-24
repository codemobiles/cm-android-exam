# CodeMobile Challenge

## สร้างโปรเจค Android แบบ Empty Activity และ Kotlin
<b>2. สร้าง Activity ขึ้นมา 3 Activity</b>
 - Login Activity
 - Home Activity
 - Detail Activity

2.1 ค่าเริ่มต้น Redirect มาหน้า Login Activity

<b>3. หน้า Login Page มี UI ดังนี้</b>

3.1 ช่อง input Email

3.2 ช่อง input Password

3.3 ปุ่มเข้าสู่ระบบ

3.4 เพิ่ม Validation

- ตรวจสอบ Format Email โดยใช้ Regex
- ตรวจสอบความรหัสผ่าน ความยาว 8 ตัวขึ้นไป
  
3.5 เมื่อกดปุ่มเข้าสู่ระบบ ตรวจสอบ Email = aa@bb.cc และ Password = 12345678 

        - ถ้าถูกต้อง Navigate ไปหน้า Home Activity
         
        - ถ้าผิดให้ Alert ข้อความ "Email or password incorrect"

<b>4. หน้า Home Activity มีเงื่อนไขตามนี้</b>

4.1 fetch ข้อมูล GET: https://dummyjson.com/products 

4.2 แปลงข้อมูล JSON ข้อ 4.1 เป็น data class (ชื่อ Product) 

4.3 แสดงข้อมูลที่ fetch ได้เป็น Card Recyclerview มีข้อมูลดังนี้
  - Thumbnail
  - Title
  - Price
  - Stock
  - ปุ่ม Detail

4.4 เมือกดปุ่ม Detail ให้ส่ง id product ผ่าน params ไปหน้า Detail Activity
 
<b>5. เพิ่ม input ช่องค้นหาข้อมูลสินค้า ค้นหาชื่อสินค้าแบบ Debound Time(1 วินาที) และ contain string ในหน้า Home Activity</b>

<b>6. เพิ่มปุ่ม Dropdown 5 เมนู ในหน้า Home Activity</b>
  - ทั้งหมด (แสดงสินค้าทั้งหมด)
  - ราคามากว่า 1000 (กรองสินค้าที่มีราคา 1000 ขึ้นไป และมี %ส่วนลด มากกว่า 0) 
  - แสดงราคารวมต่อชิ้น (เพิ่ม Column ขึ้นมาอีก 1 Column สำหรับแสดง ราคารวมต่อชิ้น) [เพิ่ม key totalPrice เข้าไปใน data class Product เพื่อแสดงใน column]
  - เรียงเรตติ้ง (เรียง rating สินค้าแบบ desc และ price แบบ asc)  
 
<b>7. หน้า Detail Activity</b>

7.1 Get id product จาก params และ fetch ข้อมูลสินค้า GET:https://dummyjson.com/products/:id   

7.2 แสดงข้อมูลสินค้า ตามสวยงาม
  - Images 150*150
  - Title
  - Price
  - Stock
  
<b>8. ปริ้นข้อความใน Life Cycle ต่างๆ ของ Activity ในหน้า Detail Page </b>

<b>9. เพิ่ม Interceptor http</b>

9.1 Add header key CMReq = “request” ตอน Request http

9.2 Add header key CMERes = “response” ตอน Response http
 
<b>10. กำหนดค่าเริ่มต้น Navigate path</b>

10.1 ถ้า ยังไม่ได้ Login ให้ Navigate มาหน้า Login Activity

10.2 ถ้า Login แล้วให้ Navigate มาหน้า Home Activity
 

# **Project 11: LCD**

### **1. Description**
Arduino I2C 1602 LCD is a commonly-used auxiliary device for MCU development board to connect with external sensors and modules. It features a 16-bit wide character and 2-line LCD screen, whose brightness is adjustable.

This programable module is convenient for data editing, displaying and managing. Besides, it can display not only characters and figures but sensors value, like temperature, humidity or pressure value.

As a result of its usability, the display is wildly applied in many fields, including smart home, industrial monitoring system, robot control and automatics' electronics.

### **2. Working Principle**

![](./media/lcd.png)

**Working Principle:** 

It is the same as IIC communication principle. Underlying functions have packaged in libraries so that you can recall them directly.

If you are interested in these, you may have a further look of underlying driving principles.

### **3. Wiring Diagram**

![09](media/09.jpg)

### **4. Test Code**

1.Drag the two basic code blocks.

2.Drag “init LCD” block from “LCD” and set the I2C address to 0x27.

![image-20230325093620843](media/image-20230325093620843.png)

3.Drag the "LCD back light" block and set it to ON. Characters are not easy to read if there is no back light.

![image-20230325093708827](media/image-20230325093708827.png)

4.Drag a "LCD cursor position" block and set x to 3 and y to 0. Add an "LCD print" block and type “keyestudio” in the blank. 

![image-20230325093952628](media/image-20230325093952628.png)

5.Again, drag another "LCD cursor position" and set x to 2 and y to 1. Add an "LCD print" and type “Hello,world!” in the blank. 

![image-20230325094043434](media/image-20230325094043434.png)

**Complete Code:**

![Img](media/img-20230308101037.png)

### **5. Test Result**

After wiring up and uploading code, turn on the LCD, and "Hello, world!" and "keyestudio!" will displayed on the LCD.

If the characters are unclear, please fix the backlight potentiometer by the small slotted screwdriver(included in this kit). Connect an external power supply if necessary.

![image-20230325091056039.png](media/image-20230325091056039.png)

### **6. Code Block Explanation**

1.Set the IIC communication address. In this project, the address of LCD 1602 is 0x27.

![Img](media/img-20230308101228.png)

2.Control the LCD back light. The displayed characters will be seen much clearly if the back light is on. 

![Img](media/img-20230308101438.png)

3.Set the cursor position. It will provide an accurate position through axis x and y. Possible values are X: 0-15 and Y: 0-1.

![Img](media/img-20230308101746.png)

4.Print characters on LCD. The blank can be filled with characters or variables, which is convenient for displaying the values from sensors and modules. 

![Img](media/img-20230308102036.png)

5.Blink the cursor at the display position. By default, the cursor is in inactive. 

![Img](media/img-20230308102320-16805113851661.png)


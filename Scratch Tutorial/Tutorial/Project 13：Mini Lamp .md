# **Project 13：Mini Lamp**

### **1. Description**
In this project, we control a lamp by Arduino UNO and a button. When we press the button, the state of the lamp will shift (ON or OFF).

### **2. Working Principle**

![](./media/img-20230225082310-1684554788483-3.png)

**Working Principle:** 

When the button is released, a voltage VCC passing through R29 provides a high level for S terminal. 

When it is pressed, pin 1 and 3, pin 2 and 4 are connected and voltage on S1 arrives GND as a low level. At this moment, R29 avoids a short circuit between VCC and GND.

### **3. Wiring Diagram**

![14](media/14.jpg)

### **4. Test Code**

1.Add two basic blocks.

2.Drag a "baud rate" from “Serial” and set it to 9600. 

![image-20230325132829253](media/image-20230325132829253.png)

3.Then drag a "print" block from “Serial”, type “Key status:” in the blank and set it to "no-warp".

![image-20230325133041424](media/image-20230325133041424.png)

4.Drag another “Serial print” block  from “Serial” and set the mode to "warp". Add a "state value of button" from “Button” and set the interface to 8.

![image-20230325133328150](media/image-20230325133328150.png)

**Complete Code:**



![13-1](media/13-1.png)

### **5. Test Result**

After wiring up and uploading code, open the serial monitor and set the baud rate to 9600. 
When we press the button, serial port prints "Key status: 0"; When we release the button, serial port prints "Key status: 1".

![image-20230318140232396](media/image-20230318140232396.png)

### **6. Expansion Knowledge**

We then will control the LED via a button.

**Flow Diagram:**

![image-20230322114827986.png](media/image-20230322114827986.png)

**Wiring Diagram:**

![10](media/10.jpg)

**Code:**

1.Drag two basic blocks. 

2.Drag a "if&else" block from “Control”. Add a "button pin" block from “Button” after "if" and set its interface to 8. 

3.Put an "LED output" block under "if" and set the output to HIGH, and put another under "else" and set to LOW. LED pins are both at 3.

![image-20230325134557767.png](media/image-20230325134557767.png)

**Complete Code:**

![13-2](media/13-2.png)

### **7. Code Block Explanation**

1.Determine whether the button is pressed. If it is, this block expresses true; If not,it is false.

![image-20230318160105218](media/image-20230318160105218.png)

2.Read the current button value. When the button is pressed, the value is 1. Or else, it is 0.

![image-20230318160315012](media/image-20230318160315012.png)

3.If the condition in the hexagon is true, "if" block will be executed. Otherwise, the program runs "else" according to block.

![image-20230318160426073](media/image-20230318160426073.png)

4.Set the baud rate. Please guarantee the serial baud rate fit the counterpart of serial monitor, or it won't print anything. The commonly used baud rate are 9600 and 115200, and here we set to 9600.

![image-20230325132829253](media/image-20230325132829253.png)

5.Print characters on serial monitor. The printed words are what you type in the blank. Besides, three print modes are included: warp, no-warp and HEX (hexadecimal). 

![image-20230325133733586](media/image-20230325133733586.png)


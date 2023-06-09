# **Project 29：IR Remote Control**
### **1. Description**
This module uses IR to remotely control LED, which greatly simplifies the ON and OFF of LED. Now that the control is realized by IR signals, there is no need to worry about considerable circuits. 

### **2. Working Principle**

![img-20230225082859](./media/img-20230225082859.png)

**Working principle:** 

In actual communication, signals usually carries a wide spectrum, and a lot of energy is distributed at a low frequency band. We called it baseband signal, which is not suitable for direct transmission in channels. 

For a convenient transmission, a high anti-disturbance capability and an effective utilization of Broadband, and signals, before transmitting, always need to be modulated to a frequency which is suitable for channels and noise characteristics. This is what we called signal modulation. 

At the receiver of the communication system, signals are usually demodulated to regain the initial baseband ones. In this project, we often use a carrier of about 38K in modulation. 

An IR remote control system is mainly split into modulation, emitting and receiving. It sends data through modulating, i.e., an "**and**" operation between data and carriers with a certain frequency. In this way, the emitting efficiency is enhanced while power dissipation is lowered. 

Generally, the frequency of carrier modulation is within 30khz~60khz, with 38kHz more often. The duty cycle of the square wave is 1/3, as shown below, which is decided by the 455kHz crystal oscillator on the emitting end. 

An Integer frequency division is essential for crystal oscillator at this end, and the frequency coefficient usually evaluates 12. Therefore, 455kHz÷12≈37.9kHz≈38kHz. 

**38KH carrier (complete) emitting diagram:**![img-20230225083510](./media/img-20230225083510.jpg)

**Carrier frequency:** 38KHz

**Wave length:**  940nm

**Receiving angle:** 90°

**Control distance:** 6M

**Schematic diagram of remote control buttons:**

![221](./media/221.jpg)

### **3. Wiring Diagram**

![31](./media/31.jpg)

### **4. Test Code**

1.Drag the two basic blocks.

2.Find and drag the "IR remote init" block from “IR Remote” and set its pin to 3. Add a "baud rate" block from "serial" and set to 9600.

![image-20230331104445825](./media/image-20230331104445825.png)

3.Drag an "if" block and fill its condition with "Received data". Only when the IR module receives data, code blocks in "if" execute.

![image-20230331104631171](./media/image-20230331104631171.png)

4.Drag another "if" block and set its condition to "Read the data ＞ 0". Only when this condition is satisfied, serial port starts to print data. 

This sensor works so fast that the code may run twice or more when you are pressing control buttons. However, the second time of a same command will send out a value of 0, so a greater-than block is necessary for the avoidance of duplication. 

![image-20230331105216727](./media/image-20230331105216727.png)

5.Add a "serial print" block after "then". Set to print the read data from "IR remote" module in the mode of "warp".

![image-20230331114809806](./media/image-20230331114809806.png)

6.In the end, do not forget to refresh data after a full execution. Otherwise, next receiving will be invalid.

![image-20230331114824593](./media/image-20230331114824593.png)

**Complete Code:**

![29-1](./media/29-1-1680247790101-55.png)

### **5. Test Result**

After wiring up and uploading code, open the serial monitor and set the baud rate to 9600. Press the button on the remote control unit, and you will see the value in hexadecimal.

![image-20230331114725348](./media/image-20230331114725348.png)

### **6. Expansion Code**

In this expansion code, we will make a light controlled by an IR remote switch. Press OK to light up the LED and press it again to turn it off. 

To realize this repeatable operation, the variable "item" is essential in the whole code. For the first time, item = 0 so codes in "else" run to assign 1 as its new value. For the second time when item = 1, however, "if" block executes to reassign to 0, alternatively.

**Wiring Diagram:**

![32](./media/32.jpg)

**Code:**


![](./media/29-2-1682213866846-7.png)



### **7. Code Block Explanation**

1.Initialize the IR remote module after setting its receiving pin.

![image-20230331131708045](./media/image-20230331131708045.png)

2.Judge whether the sensor has received data. If it is, related code blocks will run.

![image-20230331131847778](./media/image-20230331131847778.png)

3.Read the received data from IR remote control.

![image-20230331131908873](./media/image-20230331131908873.png)

4.Refresh the received data after each complete receiving execution. Or else, the next receiving will is invalid.

![image-20230331131926563](./media/image-20230331131926563.png)


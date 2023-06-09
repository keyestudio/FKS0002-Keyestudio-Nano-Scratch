# **Project 1: Blinking**

###  **1.  Description**

LED blinking is a simple project designed for starters. You only need to install an LED on Arduino board and upload the code on Arduino IDE. 

This project reinforces the learning of Arduino conceptual framework and using methods for starters. 

###  **2.  Working Principle**

![](./media/led.png)
**LED lighting principle:** 

Generally speaking, limited IO ports of output current may cause enough-less brightness of LED, so NPN triode (Q2) is applied in circuit as a switch.
In this case, the LED will light up if the base(pin 1) of triode is at a high level. On the contrary, LED goes off when the base is at low.

**Triode switch controlling principle:**

To have a clear understanding of its principle, certain knowledge of electronic circuit is required. For details, please consult materials by yourself.
Briefly, LED lights up when the base(pin 1) is at a high level. In the same breath, the collector(pin 3) and emitter(pin 2) are connected, and then VCC passes through a current-limiting resistor to LED and finally to GND, which forms a circuit. On the contrary, LED goes off when the base is at low. In this circumstance, the collector and emitter are disconnected hence the circuit is not a closed loop.

### **3.  Wiring Diagram**

![01](media/01.jpg)

###  **4.  Test Code**

According to previous principles, we can control LED via power levels of pins on the development board.

1.Drag this "when Arduino begin" block in "Events".This is one basic block. Or else, the following code blocks won't execute.

![image-20230324144129788](media/image-20230324144129788.png)

2.Drag a "forever" in "Control" to circulate the execution of the including code blocks. This is another basic block.

![image-20230324144235832](media/image-20230324144235832.png)

3.Drag an "LED output" block in "LED" and set the pin to 3 and output to HIGH.

![image-20230324144552097](media/image-20230324144552097.png)

4.Drag a delay time block in "Control" and set "wait 1 seconds".

![image-20230324144523478](media/image-20230324144523478.png)

5.Set another LED output to LOW at pin 3 as well as "wait 1 seconds".

![image-20230324144721033](media/image-20230324144721033.png)

**Complete Code:**

![img-20230307165550](media/img-20230307165550.png)


###  **5. Test Result**

After uploading the code and powering on, LED will blink alternatively of on for 1s and off for 1s.

### **6. Code Block Description**

1.Code blocks will not execute if there is no "when Arduino begin".

![Img-20230307162920](media/img-20230307162920.png)

2.Code blocks in this "forever" block will execute in a loop. 

![Img](media/img-20230307164251.png)

3.In this block, you can choose a pin to output a HIGH or LOW level. 

![Img](media/img-20230307165305.png)

4.You can type a delay time in the middle blank in the unit of seconds. 

![Img](media/img-20230307164630.png)


# **Project 2：Breathing Light**

### **1. Description**
Arduino breathing light utilizes on-board programmable PWM to output analog waveform. After powering on, LED brightness can be adjusted through duty cycle of the waveform to eventually realize a breathing light.
In this way, ambient light can be simulated by changing LED brightness along with time. Also, breathing light can form a colorful mini light show to construct a tranquil and warm environment.

### **2. PWM Working Principle**

PWM controls analog output via digital means, which are able to adjust the duty cycle of the wave (a signal circularly shifting between high level and low level).
For Arduino, digital ports of voltage output are LOW and HIGH, which respectively correspond to 0V and 5V.
Generally, we define LOW as 0 and HIGH as 1. Arduino will output 500 signals of 0 or 1 within 1s. If they are 500 "1", 5V will be output. Oppositely, if they are all 0, the output will be 0V. Or if they are 010101010101..., the average output will be 2.5V.
In other words, output ratio of 0 and 1 affects the voltage value. Honestly, it differs from real continuous output, yet the more 0 and 1 signals are output per unit time, the more accurate the control will be.

![](media/img-20230225090854.png)

### **3. Wiring Diagram**

![01](media/01-1679396611356-2.jpg)

### **4. Test Code**

We adopt "for" statement to increase a variable from 0 to 255, and we define the variable as PWM output (analogWrite(pin, value)). By the way, a delay time may reinforce the control of LED shining time. Next, we use another "for" statement to decrease it from 255 to 0 with also a delay time to control LED dimming process.
As a result, a breathing light is complete.

1.Drag the basic two code blocks.

![image-20230324145038355](media/image-20230324145038355.png)

2.Drag the following block from "Variable Type", and define the name to "item" with an initial assignment "0". Put this block in "forever". 

![image-20230324145311206](media/image-20230324145311206.png)

3.Drag a "repeat" block from "control" and set it to 255 times, which is the maximum value of PWM.

![image-20230324145621946](media/image-20230324145621946.png)

4.Drag a "Change" block from "Variable Type", put "item" as its changed object and set the mode to "++".

![image-20230324145715047](media/image-20230324145715047.png)

5.Drag an "analogWrite" from “LED” and set the LED pin to 3. Then add an "variable" block in it and fill in the blank with "item". 

![image-20230324150352779](media/image-20230324150352779.png)

6.Drag a delay time block from "Control" and set the waiting time to 0.01s = 10ms. 

![image-20230324150616342](media/image-20230324150616342.png)

7.According to previous steps, build another code block with the only difference of variable mode "– –".

![image-20230324150902217.png](media/image-20230324150902217.png)

**Complete Code:**

![Img](media/img-20230307185310.png)

### **5. Test Result**

After uploading the code, we can see the LED dims gradually rather than all of a sudden. It "breathes" evenly.
### **6. Code Block Explanation**

1.This definition block is used to set variable usable range, variable type , name and its initial value. 

![Img](media/img-20230307190132.png)

2.Repeating times can be assigned in the blank of this repeat block. 

![Img](media/img-20230307190325.png)

3.This block adds one to the variable. Input a variable name in the blank and its value will add one each time the code executing. "++" can be altered to "– –".

![Img](media/img-20230307190714.png)

4.This block suntract one from the variable. Similarly, input a variable name in the blank and its value will reduce one each time the code executing. 

![Img](media/img-20230307192056.png)

5.A certain analog output value and pins can be set in this PWM outptu block. Totally, six pins on Nano board cater for PWM, including pin 3, 5, 6, 9, 10 and 11. Besides, the analog value can be scheduled in the blank. 

![Img](media/img-20230307190828.png)


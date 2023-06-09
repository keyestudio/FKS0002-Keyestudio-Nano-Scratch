# **Project 27：Intelligent Parking**

### **1. Description**
This intelligent parking system detects and optimizes parking position via ultrasonic sensor. With this system, wrong parking is avoided to a large extent. 

Firstly, you need to install the sensor around the car-park. And then it will detect the distance between the car and its edges and send the information to the development board. After integration, the distance value will be revealed by the lines on the dot matrix display.

### **2. Flow Diagram**

![](./media/1679560585424-83.png)

### **3. Wiring Diagram**

![30](./media/30.jpg)

### **4. Test Code**

Assign the detected distance value to a variable, and judge whether it is greater than the set threshold value. If it is, corresponding lines on the dot matrix light up. In this way, a distance can be revealed by lighting lines. 

**Reference Coordinates:**

![image-20230331092241919](./media/image-20230331092241919.png)

**Complete Code:**

![27](./media/27-1680228886481-10.png)

### **5. Test Result**

After wiring up and uploading code, lines displays on the dot matrix. When the detected distance is shorter than 50cm, there are fewer lines.

![image-20230324103259033](./media/image-20230324103259033.png)![image-20230324103353015](./media/image-20230324103353015.png)


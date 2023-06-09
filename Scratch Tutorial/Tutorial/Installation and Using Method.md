# **Installation and Using Method**

## **Windows System Kidsblock Installation**

1\. Download Kidsblock package: [http://xiazai.keyesrobot.cn/KidsBlock.exe](http://xiazai.keyesrobot.cn/KidsBlock.exe)

2\. After downloading, click to open “KidsBlock 1.1.4 Setup.exe”![](./media/image-20230525120410820.png).

3\. Select “**Anyone who uses this computer(all users)**” and then click “**Next**”.

![](./media/wps2.jpg)

4\. Click “**Browse...**” to choose a path for your installation. Here we choose C Disk, of course you may choose any disk you like. Then click “**Install**”. Now the software is installing.

![](./media/image-20230425131600740.png)

![](./media/image-20230425131613363.png)

5\. After installation, click **“Finish**” to open Kidsblock.

![](./media/image-20230425131648555.png)

6\. If you PC pops up a warning interface, don't worry, just click “**Allow access**” to retry to open Kidsblock.

![](./media/image-20230425131712117.png)



## **MacOS System Kidsblock Installation:**

1\. Download Kidsblock Package: [http://xiazai.keyesrobot.cn/KidsBlock.dmg](http://xiazai.keyesrobot.cn/KidsBlock.dmg)

![](./media/image-20230425132024101.png)

2\. After downloading, click to open KidsBlock, as shown below. Then please drag **KidsBlock Desktop** into **Applications**.

![](./media/image-20230425132045495.png)

3\. Wait for the installation. When it is done, the KidsBlock icon will show up on your desktop. 

![](./media/image-20230425132102151.png)



## **Kidsblock Using Method**

(**Here we take Windows System as an example, and it is only a reference for MacOS**)

### **1. Tool Bar Description**

![](./media/image-20230425132249162.png)

### **2. Optional Language**

Click ![]./media/wps3.jpg to shift language into “English” or “简体中文”.

![](./media/image-20230425132314706.png)

### **3. Driver Installation**

**NOTE: If your computer is already installed a driver for the development board, you may skip this step. If not, please follow the following procedures.**

Click ![]./media/wps4.jpg to select “**Install driver**”.

![](./media/image-20230425132404118.png)

A. You will see the “Device Driver Installation Wizard”, please click “**Next**”.

![](./media/image-20230425132437042.png)

B. A few seconds later, the following interface pops up. Then click “**Finish**”.

![](./media/image-20230425132451000.png)

C. Click “**Next**”.

![](./media/image-20230425132508978.png)

D. And click “**Finish**”.

![](./media/image-20230425132527354.png)

E. If there is a warning, just click “**Allow**”. Then click “**Install**”.

![](./media/image-20230425132612816.png)

F. If the warning repeatedly shows up, just click “**Install**” again.

G. After a while, click “**Finish**”.

![](./media/image-20230425132706958.png)

H. Click “**Extract**”.

![](./media/image-20230425132728689.png)

I. And click “**Next**”.

![](./media/image-20230425132833120.png)

J. Click “**I accept this agreement**” and “**Next**”.

![](./media/image-20230425132909670.png)

K. Click “**Finish**”.

![](./media/image-20230425132938087.png)

L. Now click “**INSTALL**” to install the driver.

![](./media/image-20230425133212163.png)

M. Wait a moment. When the driver is successfully installed, click “**OK**”.

![](./media/image-20230425133345363.png)

### **4. Development Board Selection**

After installing the driver, open the software to enter the main page. Click ![](./media/image-20230522142513992.png) to find and select “Inventor kit for arduino”. 

![](./media/image-20230425154013289.png)

 Click “**Connect**”. After the NANO board being connected, click “**Go to Editor**”. 

![](./media/image-20230425154046009.png)

![](./media/image-20230425154112267.png)

In this way, you will find some changes on the main page:  ![](./media/image-20230425154825861.png). These imply that NANO mainboard and Port(COM are both connected. 

![](./media/image-20230425154142715.png)

### **5. Serial Port Selection**

If NANO mainboard is already connected yet ![](./media/wps12.jpg) to manually connect Port(COM. 

![](./media/image-20230425154312580.png)

Click ![](./media/wps13.jpg) to pop up an interface, and then click “**Connect**”.

![](./media/image-20230425154332273.png)

If the port is successfully connected, the following interface will show up. 

![](./media/image-20230425154353467.png)

![](./media/image-20230425154312580.png)

If you want to disconnect the port, click ![](./media/image-20230425154226277.png) to select “**Disconnect**”.

![](./media/image-20230425154444635.png)

### **6. Function Bar Description**

![](./media/20230425145556.jpg)

### **7. Sensors and Modules (Can Be Skipped)**

**NOTE: For this kit, included sensors and modules are already integrated in the device you choose (Section 4 for details), so you can ignore this step. But, if you want to add a sensor excluded in this kit, please refer to the following illustrations.**

![](./media/wps18.jpg): Add sensor/module or expansion package of components.

Click ![](./media/wps20.jpg) and “**Not loaded**” becomes “**Loaded**”. This module is successfully added! 

![](./media/wps23.jpg)

Click ![](./media/image-20230522145403429.png), as shown below.

![](./media/wps25.jpg)

If you want to remove this module, click ![](./media/wps27.jpg) again and wait for “Loaded” to become “Not loaded”.

![](./media/wps30.jpg)

We only take passive buzzer as an example. For other sensors and modules, operations are the same. 

### **8. Code File Loading**

**Method 1:** Double-click file(.SB3) to open it. For instance, directly click ![](./media/image-20230425151819813.png) to open it.

![](./media/image-20230425154545918.png)

**Method 2: **Open Kidsblock and click “**file**” to choose “**Load from your computer**”. Select a file(.SB3), like ![](./media/image-20230425151835150.png).

![](./media/image-20230425134523132.png)

![](./media/image-20230425134531074-1682408277692-1.png)

![](./media/image-20230425154658758.png)



## **Code Uploading and Baud Rate Setting**

### **1. Code Uploading**

Add file ![](./media/image-20230425155752592.png)

![](./media/image-20230425162406090.png)

![](./media/image-20230425162425434.png)

After uploading, the box under the right conner will print “Hello Keyestudio!” per second.

![](./media/image-20230425162505751.png)

### **2. Baud Rate Setting**

If the printing box is disappeared, click one of ![](./media/image-20230425160408289.png) at the upper-right conner to set.

![](./media/image-20230425160435983.png): Small printing box

![](./media/image-20230425160508513.png): Large printing box

![](./media/image-20230425160549062.png): No box

If there is a box without any prints or with garbled characters, please check the baud rate. Click ![](./media/image-20230425160732792.png) to set the baud rate to the same as codes, that is 9600.

![](./media/image-20230425160917098.png)


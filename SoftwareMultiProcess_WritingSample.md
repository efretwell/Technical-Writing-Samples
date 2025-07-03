# “Database is currently in Single User Mode or is Unavailable. This application will be shut down” error message when attempting to start *Company Software*

**SYMPTOMS**

When you try to start *Company Program*, the following error message appears:

Database is currently in Single User Mode or is Unavailable. This application will be shut down. Please call Customer Support.

**CAUSE**

This issue can occur if any of the following are true:

* The Microsoft SQL Server Desktop Engine (MSDE) service is not started.  You must start the MSDE service before starting the program.  
* *Company Software* Individual, *Company Software* Manager, or *Company Software* FastFile is starting in Compatibility Mode. Turn off Compatibility Mode before starting the program.  
* The user attempting to start the program is not logged in to Microsoft Windows with administrator access. Log in to Microsoft Windows with administrator access before starting the program.  
* The host computer name has changed after installing the program. If the computer name has changed, see Method 3\.  
* The database has been set to Single User Mode.

**RESOLUTION**

**Method 1: Start the Microsoft SQL Server Desktop Engine (MSDE) Service**

To start MSDE, follow these steps:

1. From the host computer **Start** menu, go to **All Programs** \> **Startup** \> **Service Manager**.  
2. Select the **Start/Continue** button and then try to start the *Company Software* program.

**Method 2: Repair the Installation**

To repair the installation, follow these steps:

1. Close all open programs.  
2. Place the *Company Software* installation CD in your CD-ROM drive.   
   1. If the AutoPlay feature is enabled, setup begins automatically.   
   2. If Setup does not start automatically, go to **My Computer**, right-click your CD drive and then select **AutoPlay**.  
3. Select **Repair** and then select **Next**. Setup detects and repairs the installation of the program.  
4. Select **Finish** to complete the repair.  
5. Open and start *Company Software*.

**Method 3: Uninstall and Reinstall Microsoft SQL Server Desktop Engine (MSDE)**

To uninstall and reinstall MSDE, follow these steps:

1. From the **Start** menu, open the **Control Panel** and then double-click **Add or Remove Programs**.  
2. Select **Microsoft SQL Server Desktop Engine** and then select **Remove**.   
   **Note:** It may take up to 15 minutes to remove MSDE.  
3. Select the *Company Software* program experiencing the error and then select **Remove**.  
4. Reinstall the program experiencing the error (*Company Software*  Individual, *Company Software* Manager, or *Company Software* FastFile). MSDE will be installed with the program.

	See the following Knowledge Base article for information on installing *Company Software* :  
		  
		[24035024 How to Install Company Software](http://www.)

**Method 4: Turn off Single User Mode**

To turn off Single User Mode, follow these steps:

1. From the **Start** menu, open **Run**,   
2. In the **Open** text field, enter the following command and then select **OK**:   
   explorer   
3. Locate the following folder, where drive is the drive on which the program is installed and year is the year of the program experiencing the issue: \[drive\]:  
   \\Program Files\\*Company Software*\\\[year\]  
4. Double-click **DB\_SetSingleUserOFF.exe**.  
5. In the **Select Products** box, select the product experiencing the error and then select **OK**.  
6. Select **Check here to change mode to multi-user**, select **OK**, and then select **OK**.

**Method 5: Turn Off Compatibility Mode**

To turn off Compatibility Mode, follow these steps:

1. Right-click the shortcut you use to open the *Company Software* program and then select **Properties**.  
2. Select the **Compatibility** tab, clear the checkbox to **Run this program in compatibility mode**, and then select **OK**.

**MORE INFORMATION**

Uninstalling *Company Software* Individual, *Company Software* Manager, *Company Software* FastFile, or MSDE does not remove any tax returns or database information.

**APPLIES TO**

* *Company Software* Individual  
* *Company Software* Manager  
* *Company Software* FastFile


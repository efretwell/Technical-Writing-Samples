# “Error 1325 – *Company* is not a valid short file name” error message appears when attempting to install *Company Software*

**SYMPTOMS**

When you try to install *Company Software*, the following error message appears:

	Error 1325 – *Company* is not a valid short file name

**CAUSE**

This issue can occur if your computer does not have a c: drive. Setup copies files to your c: drive during *Company Software* installation.  
	  
**RESOLUTION**

To resolve the issue, follow these steps:

1. Go to the **Start** menu and open **Run**.   
2. In the **Open** field, enter the following command and then select **OK**:  
   cmd  
3. In the **Command Prompt** enter the following, where \[drive\] is the letter of the drive where Windows is installed, and then select **Enter**:  
   drive:  
4. Type mkdir drivec and then select **Enter**.  
5. Type subst c: drivec and then select **Enter**.  
6. Try installing *Company Software*.

**APPLIES TO**

* *Company Software* Individual  
* *Company Software* Manager  
* *Company Software* FastFile


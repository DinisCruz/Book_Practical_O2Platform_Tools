##  Util - Windows Handles Viewer (Simple Gui) v1.0.exe 

Following my research into [Win32 Messaging APIs](http://diniscruz.blogspot.com/2012/11/good-resources-on-user32dll-windows.html) that allowed me to put both [IBM AppScan Source and Standard working side by side](http://diniscruz.blogspot.co.uk/2012/11/ibm-appscan-sources-and-appscan.html) and to [connect TeamMentor with AppScan Source](http://diniscruz.blogspot.co.uk/2012/11/jni4net-part-4-integrating-appscan-with.html), here is a pretty sweet **Windows Handles Viewer **which allows the easy discovery (and in some cases modification) of the Window's Handle of a particular Win32's Button, TextBox, Menu, Window, etc...

You can download this (857kb) .NET 4.0 app from [Util - Windows Handles Viewer (Simple Gui) v1.0.exe](https://dl.dropbox.com/u/81532342/O2Platform%20Tools/Windows/Windows_Messages/Util%20-%20Windows%20Handles%20Viewer%20%28Simple%20Gui%29%20v1.0.exe)  


And this is what it looks like:

[![](images/CropperCapture_5B8_5D.jpg)](http://1.bp.blogspot.com/-sRm9ISHBccY/UKuQ55bxCTI/AAAAAAAACXc/jsxLqJl2MDs/s1600/CropperCapture%5B8%5D.jpg)

  


  
To find a handle, just drag the **_Target_** **_icon _**around and you will see the values in the **_Handle_**, **_Window _**and _Handle Text_ change.

In the image below, the **_Target _**_**icon **_was hovering on top of this tools's top bar:

[![](images/CropperCapture_5B11_5D.jpg)](http://4.bp.blogspot.com/-xT6fyZONQpE/UKuRy0JZk3I/AAAAAAAACXk/Rm3mXxW5oAI/s1600/CropperCapture%5B11%5D.jpg)

  


The _Handle Text _TextBox can also be used to edit the value (which if applicable will be changed on the target Handle):

  


[![](images/CropperCapture_5B13_5D.jpg)](http://4.bp.blogspot.com/-KacdL7c392Q/UKuSDql3-rI/AAAAAAAACXs/kpCGR1n_N70/s1600/CropperCapture%5B13%5D.jpg)

  


We can also view and edit other process (like Notepad)

  


[![](images/CropperCapture_5B14_5D.jpg)](http://4.bp.blogspot.com/-1FOb2CBw9cI/UKuTexgKMHI/AAAAAAAACYM/DAJ5xdGJBmM/s1600/CropperCapture%5B14%5D.jpg)

  
And even Chrome:

[![](images/CropperCapture_5B15_5D.jpg)](http://1.bp.blogspot.com/-3dQjJRGrCcE/UKuTMaUIjsI/AAAAAAAACX0/38pZp7XGCjE/s1600/CropperCapture%5B15%5D.jpg)

  
In the example below, note how the the URL was changed, but the loaded website is still the same (owasp.org)

[![](images/CropperCapture_5B17_5D.jpg)](http://1.bp.blogspot.com/-fSuSAEV-WBg/UKuTNpavEaI/AAAAAAAACYA/YxGfYZzS6s0/s1600/CropperCapture%5B17%5D.jpg)

NOTE: These _'handle detection'_ and _'set text'_ techniques don't work with all visible controls:

  * more complex Windows controls, like TreeViews, DataGridViews, RichTextBoxes, ListViews, etc... require more complex Windows Messages
  * a number of applications, like for example WPF applications or WebBrowsers, have their own rendering engine (i.e. not using Win32/user32.dll )

    * in this case we will only see a handle for the window hosting those rendering engines

**Script this tool: **If you want to run or modify this tool (using the [O2 Platform](http://diniscruz.blogspot.co.uk/p/owasp-o2-platform.html)) here is the script used to create it: [Util - Windows Messages Handle Viewer (Simple Gui).h2](https://github.com/o2platform/O2.Platform.Scripts/blob/master/APIs/Windows/Windows_Messages_Tools/Util%20-%20Windows%20Messages%20Handle%20Viewer%20(Simple%20Gui).h2)

**Credits:** this tools re-uses code from the [http://hawkeye.codeplex.com/](http://hawkeye.codeplex.com/) tool

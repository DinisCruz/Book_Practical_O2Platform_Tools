##  Showing Chrome, Eclipse, IBM AppScan Standard and VisualStudio in the same Process/Window 

  
**UPDATE (Jan/13): **See [PoC - Selenium - Gui with 3 Hijacked Browser Windows.h2](http://blog.diniscruz.com/2013/01/poc-selenium-gui-with-3-hijacked.html) post for another powerful example of consuming Chrome (and IE and Firefox) window in another process  


* * *

Using the control shown in [Util - Win32 Window Handle Hijack (4x host panels)](http://diniscruz.blogspot.com/2012/11/util-win32-window-handle-hijack-4x-host.html) I was able to create a process that has windows from:

  * **Chrome **(top left)
  * **Eclipse **(top right)
  * **IBM AppScan Standard** (bottom left)
  * **VisualStudio **(bottom right)

  


  


[![](images/CropperCapture_5B7_5D.jpg)](http://2.bp.blogspot.com/-IQacmak7pvU/ULbMcuAb5dI/AAAAAAAAF6A/I8xSUSI0Z1o/s1600/CropperCapture%5B7%5D.jpg)

**Chrome inside Eclipse**

We can also 'push' windows into other controls.

For example, here is a Chrome Browser window running inside Eclipse (note that the TeamMentor window on the top-right is being executed by Chrome's process (not eclipse))

[![](images/CropperCapture_5B8_5D1.jpg)](http://2.bp.blogspot.com/-MAGikiJRP5Y/ULbMququEVI/AAAAAAAAF6I/OrhqHpjk56w/s1600/CropperCapture%5B8%5D.jpg)

**Chrome inside IBM AppScan Standard:**  
**  
**In the example below, TeamMentor is also hosted by Chrome, while being shown natively on AppScan's GUI:

[![](images/CropperCapture_5B9_5D.jpg)](http://3.bp.blogspot.com/-fltqF1w2aLQ/ULbNUe0qFrI/AAAAAAAAF6Q/yr3yaXxLdeQ/s1600/CropperCapture%5B9%5D.jpg)

  


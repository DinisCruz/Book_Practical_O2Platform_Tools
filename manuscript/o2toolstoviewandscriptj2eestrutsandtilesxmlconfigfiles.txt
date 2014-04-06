##  O2 tools to view and script J2EE, Struts and Tiles xml config files 

If you are reviewing Java/J2EE applications, here are a number of mini O2 tools that will help you to understand what is going on:

  * [Util - View Struts Mappings v.1.0.exe](https://dl.dropbox.com/u/81532342/O2Platform%20Tools/Java/Util%20-%20View%20Struts%20Mappings%20v.1.0.exe) (4.7Mb)
  * [Util - View struts-config.xml mappings v1.0.exe](https://dl.dropbox.com/u/81532342/O2Platform%20Tools/Java/Util%20-%20View%20struts-config.xml%20mappings%20v1.0.exe) (817kb)
  * [Util - View tiles-def.xml mappings v1.0.exe](https://dl.dropbox.com/u/81532342/O2Platform%20Tools/Java/Util%20-%20View%20tiles-def.xml%20mappings%20v1.0.exe) (816kb)
  * [Util - View validation.xml mappings v1.0.exe](https://dl.dropbox.com/u/81532342/O2Platform%20Tools/Java/Util%20-%20View%20validation.xml%20mappings%20v1.0.exe) (817kb)
  * [Util - View Web.Xml mappings v1.0.exe](https://dl.dropbox.com/u/81532342/O2Platform%20Tools/Java/Util%20-%20View%20Web.Xml%20mappings%20v1.0.exe) (817kb)

  


Bellow are these Tools in action (using the demo apps from [struts-1.3.10-all.zip](http://apache.mirrors.timporter.net//struts/binaries/struts-1.3.10-all.zip) )

**Util - View Struts Mappings v.1.0**  
**  
**Drop in the TreeView (white space) the WEB-INF folder

[![](images/CropperCapture_5B19_5D.jpg)](http://1.bp.blogspot.com/-x_XHqj9iFB8/UJ1B-tn-qGI/AAAAAAAAB-o/pVweypVZcXM/s1600/CropperCapture%5B19%5D.jpg)

  
This control will load up the web.xml, struts-config.xml, tiles-def.xml and validation.xml config files, and create a **_mapping view_** of that data

The reason this exe is 4Mbs is because it includes the C# REPL script environment

[![](images/CropperCapture_5B21_5D.jpg)](http://1.bp.blogspot.com/-PJhwowLBKm4/UJ1DkamQyiI/AAAAAAAAB-w/twxAvzbLBgg/s1600/CropperCapture%5B21%5D.jpg)

  


  


Which can be used to access/script the **_StrutsMappings_** object created (and visualized in the TreeView shown above)

  


[![](images/CropperCapture_5B22_5D.jpg)](http://4.bp.blogspot.com/-IlPTjjxRYYo/UJ1Dlfx649I/AAAAAAAAB-0/ZWZTL5HlqKo/s1600/CropperCapture%5B22%5D.jpg)

  
The _code sample_ menu item, shows how to easily access the the mapped Struts data:

[![](images/CropperCapture_5B23_5D.jpg)](http://3.bp.blogspot.com/-DRp1KadJ-Cc/UJ1EPbrcVjI/AAAAAAAAB_A/99NGufy9Eso/s1600/CropperCapture%5B23%5D.jpg)

  
The _REPL Form_ menu item, provides access the _Form _object which (for example) can be used to make all child controls pink :)

[![](images/CropperCapture_5B24_5D.jpg)](http://2.bp.blogspot.com/-3dDlZG0-0kU/UJ1ErcWVoVI/AAAAAAAAB_I/VdHHdKyQGdI/s1600/CropperCapture%5B24%5D.jpg)

**Util - View struts-config.xml mappings v1.0.exe**

Drop the struts-config.xml file to see its mappings:

[![](images/CropperCapture_5B25_5D.jpg)](http://2.bp.blogspot.com/-Y5iPWLcgQ4s/UJ1G1lJGBbI/AAAAAAAAB_Q/h9ph2pgu1KI/s1600/CropperCapture%5B25%5D.jpg)

**  
****Util - View tiles-def.xml mappings v1.0.exe**

Drop the tiles-defs.xml file to see its mappings:

[![](images/CropperCapture_5B26_5D.jpg)](http://4.bp.blogspot.com/-q6Epc4n9Sps/UJ1G2rTJzOI/AAAAAAAAB_U/gfqhcHSD4JQ/s1600/CropperCapture%5B26%5D.jpg)

**  
****Util - View validation.xml mappings v1.0.exe**  
Drop the validation.xml file to see its mappings:  
**  
**  


[![](images/CropperCapture_5B27_5D.jpg)](http://1.bp.blogspot.com/-H5oEN9xxoL0/UJ1G3IU4SkI/AAAAAAAAB_c/o5dQ6il-3xk/s1600/CropperCapture%5B27%5D.jpg)

**  
****  
****Util - View Web.Xml mappings v1.0**  
**  
**Drop the web.xml file to see its mappings:

[![](images/CropperCapture_5B28_5D.jpg)](http://2.bp.blogspot.com/-f8L0CGQrvi4/UJ1G4ZtZAHI/AAAAAAAAB_o/zoe3RlTUNx4/s1600/CropperCapture%5B28%5D.jpg)

If you like this (and are reviewing Java Apps with lots of interfaces) you should also check out the [Util - O2 Java Tools (IKVM Based) v1.0](http://diniscruz.blogspot.com/2012/10/util-o2-java-tools-ikvm-based-v10.html)

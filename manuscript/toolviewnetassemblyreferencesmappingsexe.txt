##  Tool - View .NET Assembly References Mappings.exe 

Here is a 'simple' .Net mini-tool that shows two TreeViews with .Net assemblies reference's dependencies (I used it today to figure out how many dependencies a particular dll had).

You can download this [O2 Platform](http://blog.diniscruz.com/p/owasp-o2-platform.html) tool from: [Tool - View .NET Assembly References Mappings.exe](https://dl.dropbox.com/u/81532342/O2Platform%20Tools/dotNet/Tool%20-%20View%20.NET%20Assembly%20References%20Mappings.exe) (5Mb)

**Here is what it looks when executed for the first time:**

[![image](images/image_thumb1.png)](http://lh5.ggpht.com/-7jiXC4JGn_g/URPuasRvorI/AAAAAAAAI9Y/eC-ibsO6Q10/s1600-h/image%25255B2%25255D.png)

On the left you have the original assembly (in this can the actual **_[Tool - View .NET Assembly References Mappings.exe](https://dl.dropbox.com/u/81532342/O2Platform%20Tools/dotNet/Tool%20-%20View%20.NET%20Assembly%20References%20Mappings.exe)_**) and the dlls it depends on.

On the right you have the XRef mappings of each assembly loaded on the right:

[![image](images/image_thumb_25255B1_25255D1.png)](http://lh4.ggpht.com/-rJ8Ynscio6Q/URPueD4ADOI/AAAAAAAAI9k/yXXrGl2gUiI/s1600-h/image%25255B5%25255D.png)

Where this gets interesting is if you drop a folder into the left-hand-side **_TreeView_**:

[![image](images/image_thumb_25255B2_25255D.png)](http://lh3.ggpht.com/-lu11Uaupfqw/URPuhJdzQPI/AAAAAAAAI90/iZH0XQAPiVM/s1600-h/image%25255B8%25255D.png)

All dlls are loaded (on the left) and the XRefs (on the right) show more mappings:

[![image](images/image_thumb_25255B3_25255D1.png)](http://lh4.ggpht.com/-Vts2xs8v7t4/URPukcvPJ8I/AAAAAAAAI-E/wUPJ3UTVp1g/s1600-h/image%25255B11%25255D.png)

The loading and mapping of dlls is very quick, for example it took about 2 seconds to load and map 81 assemblies:

[![image](images/image_thumb_25255B4_25255D.png)](http://lh3.ggpht.com/-A-yuYDaXIJ8/URPun7bg3pI/AAAAAAAAI-U/Ga2EL-dZ2So/s1600-h/image%25255B14%25255D.png)

The '**_REPL Selected Assembly'_****_ ToolStrip Button_**, will open a [C# REPL](http://blog.diniscruz.com/p/c-repl-script-environment.html) for the assembly selected (on the left **_TreeView_**)

For example here is the **_AWSSDK.dll_** assembly:

[![image](images/image_thumb_25255B5_25255D.png)](http://lh3.ggpht.com/-CAOaJ8w-sbQ/URPurSHGD-I/AAAAAAAAI-o/zgelyn0AVlA/s1600-h/image%25255B17%25255D.png)

Once we have a dll loaded,  we can (for example) list it classes using reflection:

[![image](images/image_thumb_25255B6_25255D.png)](http://lh4.ggpht.com/-ybLjyyWhb60/URPuudjPZPI/AAAAAAAAI-4/_YdLiHWG9_I/s1600-h/image%25255B20%25255D.png)

**Note 1: **you probably noticed that I used and packaged ILSpy (in order to use Mono.Cecil) as one of the dependencies, so a cool improvement of this script would be to fire up ILSpy from here, or even better to show its main decompilation GUI (TreeView and decompiled code).

**Note 2: **The script that created this tools is at GitHub: [Tool - View .NET Assembly References Mappings.h2](https://github.com/o2platform/O2.Platform.Scripts/blob/8c28865ed5a82357c84d8ddedb699dc5ea33a56a/Languages/DotNet/Mono_and_Reflection/Tool%20-%20View%20.NET%20Assembly%20References%20Mappings.h2)

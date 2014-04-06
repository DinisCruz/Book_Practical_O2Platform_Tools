##  Packaging an O2 Platform Script as a stand alone tool (in this case the WatiN based 'IE Script' tool) 

If you grab the latest version of the [O2 Platform](http://blog.diniscruz.com/p/owasp-o2-platform.html) and try to run the _**IE Script **_tool

[![image](images/image_thumb_25255B9_25255D.png)](http://lh3.ggpht.com/-XtgFIt8nd6A/UUMrEe8iHcI/AAAAAAAAK3c/jkgf7B2HNoc/s1600-h/image%25255B4%25255D.png)

you might get a bunch of compilation errors, like the ones Arnaud described in this [How to get a "full" version of o2](http://lists.owasp.org/pipermail/owasp-o2-platform/2013-March/000449.html)  mailing list thread.

The best way to deal with this is to run this O2 Script as a 'packaged script', i.e. from a stand-alone exe that contains all dependencies required to run it.

**The rest of this post shows how to create such stand-alone exe for the _IE Script_ tool.**

Open the **_Package O2 Script_** tool/script

[![image](images/image_thumb_25255B24_25255D.png)](http://lh5.ggpht.com/-xFzbDG3d2l0/UUMrHbOoQGI/AAAAAAAAK3s/sxxr58LKpbA/s1600-h/image%25255B10%25255D.png)

which looks like this:

[![image](images/image_thumb_25255B25_25255D.png)](http://lh4.ggpht.com/-uZlJc3bk5OY/UUMrKBbIBsI/AAAAAAAAK38/klRNtXBLO78/s1600-h/image%25255B13%25255D.png)

Then click on **_Find an O2 Script_**:

[![image](images/image_thumb_25255B26_25255D.png)](http://lh5.ggpht.com/-IPQnysKC1FU/UUMrMSxMuII/AAAAAAAAK4M/uoQcNQNnqQo/s1600-h/image%25255B16%25255D.png)

Search for **_IE Automation_**  
**_  
_**[![image](images/image_thumb_25255B27_25255D.png)](http://lh3.ggpht.com/-R6NSQxEBWL4/UUMrOTMiw9I/AAAAAAAAK4c/eFb9l1m41_s/s1600-h/image%25255B19%25255D.png)

And Drag-n-drop the **_IE Automation (Simple mode).h2_**  into the _Drop Zone_  
_  
_[![image](images/image_thumb_25255B33_25255D.png)](http://lh3.ggpht.com/-aNosyUd7FBA/UUMrQufVz2I/AAAAAAAAK4s/O0lMunD6iy0/s1600-h/image%25255B23%25255D.png)

The button should go green to represent an active build/package process

[![image](images/image_thumb_25255B34_25255D.png)](http://lh4.ggpht.com/-uOnbvYl1jOI/UUMrS9vFR_I/AAAAAAAAK48/gz5t8GA29sk/s1600-h/image%25255B26%25255D.png)

And look like this when completed (the button goes red if there are compilation or packaging errors)

[![image](images/image_thumb_25255B35_25255D.png)](http://lh4.ggpht.com/-IbZQJqzhpak/UUMrVbmDpDI/AAAAAAAAK5M/_IvIl5uEjfI/s1600-h/image%25255B29%25255D.png)

That **_3.084kb_** exe file is now our packaged script :)

You can run this executable directly from here:

[![image](images/image_thumb_25255B36_25255D.png)](http://lh6.ggpht.com/-h8vjnm7kQZU/UUMrYKIChOI/AAAAAAAAK5c/bcNWSptwyvc/s1600-h/image%25255B32%25255D.png) 

or copy it to another vm with .NET 4.0 installed

[![image](images/image_thumb_25255B37_25255D.png)](http://lh4.ggpht.com/-fR0VrMIMkrA/UUMrauiGvpI/AAAAAAAAK5s/pFQkPITAFhw/s1600-h/image%25255B35%25255D.png)

and run it from there:

[![image](images/image_thumb_25255B38_25255D.png)](http://lh4.ggpht.com/-WM9_eDErBlw/UUMrc6u1UVI/AAAAAAAAK58/V1KYnE0zXkM/s1600-h/image%25255B38%25255D.png)

In some cases (like this one), there will be two new folders created in the executable folder.

The **_O2.Platform.Scripts_** (containing the scripts dynamically compiled by the REPL)

[![image](images/image_thumb_25255B39_25255D.png)](http://lh6.ggpht.com/-y2SfaArBmPY/UUMrfcV9i0I/AAAAAAAAK6M/sJW0t7gUpLU/s1600-h/image%25255B41%25255D.png)

And the **_O2.Temp_** (which will contain all temp files (including the O2 assemblies that were embedded in the stand-alone exe and extracted to facilitate the compilation))

[![image](images/image_thumb_25255B41_25255D.png)](http://lh3.ggpht.com/-aFaw2nsJQG8/UUMriWaqCRI/AAAAAAAAK6c/aau9ahlmhzU/s1600-h/image%25255B47%25255D.png)

Going back into the tool that created the stand alone script, the logs provide really good info on what happened:

[![image](images/image_thumb_25255B42_25255D.png)](http://lh5.ggpht.com/-5JsnFEewA8g/UUMrkzE-wXI/AAAAAAAAK6s/HmMP1libufY/s1600-h/image%25255B50%25255D.png)

and if you open the **__BuildFiles_** you can see the VisualStudio project that was programmatically created and compiled

[![image](images/image_thumb_25255B43_25255D.png)](http://lh4.ggpht.com/-pOt8i8cpkcM/UUMrowgpTwI/AAAAAAAAK68/AnA454ralj4/s1600-h/image%25255B53%25255D.png)

In fact, you can open that **_IE Automation (Simple mode).csproj_** file in VisualStudio

[![image](images/image_thumb_25255B44_25255D.png)](http://lh4.ggpht.com/-EfBV_ER9S5E/UUMrrb-_cbI/AAAAAAAAK7M/0ZXusB7b0t0/s1600-h/image%25255B56%25255D.png)

And run the tool (or a customized version of it) from there:

[![image](images/image_thumb_25255B46_25255D.png)](http://lh3.ggpht.com/-7duYPtKyEpI/UUMrt748HUI/AAAAAAAAK7c/buHW66yIyjE/s1600-h/image%25255B62%25255D.png)

Note: I just uploaded the **_IE Automation (Simple mode) v1.0.exe_** tool to the [O2 Platform downloads at Google Code](https://code.google.com/p/o2platform/downloads/list), so you can also [grab it from there](https://o2platform.googlecode.com/files/IE%20Automation%20%28Simple%20mode%29%20v1.0.exe):

[![image](images/image_thumb_25255B47_25255D.png)](http://lh3.ggpht.com/-e5djcjUgWWo/UUMrwvO92II/AAAAAAAAK7s/rzJ33Ls4jsQ/s1600-h/image%25255B65%25255D.png)

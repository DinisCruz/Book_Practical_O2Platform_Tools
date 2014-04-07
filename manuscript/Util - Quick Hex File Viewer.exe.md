##  Util - Quick Hex File Viewer.exe 

When I was creating the [Generating Fuzzing Images and trying them on WebBrowser (IE)](http://blog.diniscruz.com/2013/08/generating-fuzzing-images-and-trying.html)  and [Install Debugging Tools for Windows as a Standalone Component](http://blog.diniscruz.com/2013/08/install-debugging-tools-for-windows-as.html) scripts I needed a simple and fast HEX viewer.

Since I didn't had one at hand, I quickly wrote an O2 Script that uses a C# ListView to show binary data (see [source code](https://gist.github.com/DinisCruz/6246348) below)

Here is the link to the Stand-Alone tool: [Util - Quick Hex File Viewer v1.0.exe](https://dl.dropboxusercontent.com/u/81532342/O2Platform%20Tools/Windows/Util%20-%20Quick%20Hex%20File%20Viewer%20v1.0.exe)

Which looks like this when executed:  
  
 [![image](images/image_thumb_25255B1_25255D1.png)](http://lh5.ggpht.com/-jhTjTFQr_CU/Ug17fDA7dcI/AAAAAAAAPIk/v4exk_Ld8YY/s1600-h/image%25255B5%25255D.png)

... like this after a binary file is dropped inside it:

[![image](images/image_thumb_25255B4_25255D1.png)](http://lh4.ggpht.com/-yK6_yeQ9kpo/Ug17ie_JLOI/AAAAAAAAPI0/1RIc34KUsBM/s1600-h/image%25255B14%25255D.png)

... and like this after a text file is dropped inside it:

[![image](images/image_thumb_25255B5_25255D1.png)](http://lh3.ggpht.com/-mpqSznIvu7s/Ug17lWc0rmI/AAAAAAAAPJA/OIo18NKC_1U/s1600-h/image%25255B17%25255D.png)

**Here i[s the script](https://gist.github.com/DinisCruz/6246348) that creates this tool:**  
(also included in the O2.Platform.Scripts repository as _Util - Quick Hex File Viewer v1.0.h2_)

  
    
Finally here is the moment I uploaded the packaged stand-alone exe to dropbox (which is the location of the [direct link](https://dl.dropboxusercontent.com/u/81532342/O2Platform%20Tools/Windows/Util%20-%20Quick%20Hex%20File%20Viewer%20v1.0.exe) to this tool)

[![image](images/image_thumb1.png)](http://lh6.ggpht.com/-fZUi09KsF0M/Ug17oXInAMI/AAAAAAAAPJQ/ccvIfF-Xjl4/s1600-h/image%25255B2%25255D.png)

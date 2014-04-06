##  WinDbg, Cdb, Sun-Of-Strike and Util - Start SoSNet (O2 Version).exe 

If you are want to manipulate or analyze a .Net in real time, one of the best options is to use the .Net debugging API, and the best way to do that is to use the cdb.exe utility ([downloadable from here](http://msdn.microsoft.com/en-us/windows/hardware/gg463009/)) with the SoS (Sun-Of-Strike) managed debugger extension

A while back I found the SoSNet project (which was a gui on top of Sos) from [https://bitbucket.org/grozeille/sosnet](https://bitbucket.org/grozeille/sosnet) which I then forked into [https://github.com/o2platform/O2_Fork_SoS_Net/](https://github.com/o2platform/O2_Fork_SoS_Net/) in order to allow it to compile under Roslyn (and add a couple other changes/fixes)

If you want to give this tool a test drive here is an stand-alone exe: [Util - Start SoSNet (O2 Version) v1.0.exe](https://dl.dropbox.com/u/81532342/O2Platform%20Tools/dotNet/Util%20-%20Start%20SoSNet%20%28O2%20Version%29%20v1.0.exe) (created from the _Util - Start SoSNet (O2 Version).h2 _script), which you can see in action at the end of this post.  


If you don't know (or have used) SoS, you are missing a massive trick!!! You will get FULL access to the CLR, and there is no .Net object that you can't access (or manipulate). It is spectacularly powerful, and you will never do .Net debugging the same way again. And with the O2 modules/tools and the [SunOfStrikeAPI.cs](https://github.com/o2platform/O2.Platform.Scripts/blob/master/Languages/DotNet/SoS/SunOfStrikeApi.cs) , it can now be scripted in a REPL environment :)

See the [Scripting SoS (Sun-of-Strike) .Net managed extension using O2](http://diniscruz.blogspot.co.uk/2012/11/scripting-sos-sun-of-strike-net-managed.html)  post for detailed examples on how to script SoS in a real-time REPL environment (you might also like the [Scripting MDbg and DbgHostLib](http://diniscruz.blogspot.co.uk/2012/11/scripting-mdbg-and-dbghostlib.html) post).

For more on SoS see:  


  * [SOS Debugging Extension v2.0 (SOS.dll)](http://msdn.microsoft.com/en-us/library/bb190764(v=vs.80).aspx) and [SOS.dll v.4.0 (SOS Debugging Extension)](http://msdn.microsoft.com/en-us/library/bb190764(v=VS.100).aspx) 
  * [SoS cheatsheet](http://geekswithblogs.net/.NETonMyMind/archive/2006/03/14/72262.aspx) 
  * [Sending an SOS](http://codenasarre.wordpress.com/2011/06/22/sending-an-sos/) 
  * [Special Command---Editing memory with a, eb, ed, ew, eza, ezu](http://blogs.msdn.com/b/debuggingtoolbox/archive/2010/01/06/special-command-editing-memory-with-a-eb-ed-ew-eza-ezu.aspx) 
  * [Updating .NET String in memory with Windbg](http://naveensrinivasan.com/2011/06/14/updating-net-string-in-memory-with-windbg/) 
  * [How to set breakpoint in windbg for managed code](http://asher2003.wordpress.com/2010/08/11/how-to-set-breakpoint-in-windbg-for-managed-code/) 
  * [Setting breakpoints in .net code using !bpmd](http://blogs.msdn.com/b/tess/archive/2008/04/28/setting-breakpoints-in-net-code-using-bpmd.aspx) 
  * [Get Started: Debugging Memory Related Issues in .Net Application Using WinDBG and SOS](http://www.codeproject.com/Articles/23589/Get-Started-Debugging-Memory-Related-Issues-in-Net) 
  * [http://netinverse.com/devblogs/sos-son-of-strike/](http://netinverse.com/devblogs/sos-son-of-strike/) (lots of SoS posts)
  * [The Immediate Window: Running WinDbg and SOS (Son of Strike) Commands](http://blogs.msdn.com/b/zainnab/archive/2010/09/30/the-immediate-window-running-windbg-and-sos-son-of-strike-commands-vstiptool0097.aspx) (if you are using Visualstudio)
  * [Debugging .NET 4.0 applications using SOS extension](http://www.dotnetcurry.com/ShowArticle.aspx?ID=648) 
  * [Son of Strike (SOS)](http://etutorials.org/Programming/programming+microsoft+visual+c+sharp+2005/Part+IV+Debugging/Chapter+13+Advanced+Debugging/Son+of+Strike+SOS/) (old but lots of good examples of SoS commands in action) 
  * [SOS -- "Son of Strike"](http://www.develop.com/media/pdfs/developments_archive/SOS.pdf) by Mark Smith

A related technique is the one show in the [Video: Injecting C# DLLs into Managed (C#) and Unmanaged (C++) processes](http://diniscruz.blogspot.co.uk/2012/06/video-injecting-c-dlls-into-managed-c.html) (where .Net assemblies are injected into another .NET process)

  
**Screenshots of [Util - Start SoSNet (O2 Version) v1.0.exe](https://dl.dropbox.com/u/81532342/O2Platform%20Tools/dotNet/Util%20-%20Start%20SoSNet%20%28O2%20Version%29%20v1.0.exe) in action:**  
**  
**Default Gui (note the extra O2 Menu and REPL script below)  
**  
**  


[![](images/CropperCapture_5B89_5D.jpg)](http://3.bp.blogspot.com/-ioCAadWLIZk/UJNfBQ6qpFI/AAAAAAAABJI/m0uQYegYJn8/s1600/CropperCapture%5B89%5D.jpg)

  


 Listing current processes and selecting an .Net process to attach

[![](images/CropperCapture_5B91_5D.jpg)](http://3.bp.blogspot.com/-mC2Exz87Iz4/UJNfDmZOKYI/AAAAAAAABJU/kXFL_JCXpDM/s1600/CropperCapture%5B91%5D.jpg)

  
Once attached you can see a list of AppDomains (which you can select one)

[![](images/CropperCapture_5B92_5D.jpg)](http://1.bp.blogspot.com/-LcDdMnDvUe4/UJNfEa0ZwEI/AAAAAAAABJc/Vm3wrcoQC6w/s1600/CropperCapture%5B92%5D.jpg)

  
Here is the list of loaded assemblies

[![](images/CropperCapture_5B93_5D.jpg)](http://1.bp.blogspot.com/-pTfsdYZ_YKU/UJNfFpewBuI/AAAAAAAABJk/LTOLo36be3E/s1600/CropperCapture%5B93%5D.jpg)

  
Here are the current types in the selected AppDomain

[![](images/CropperCapture_5B94_5D.jpg)](http://4.bp.blogspot.com/-SBHCYQfAKCM/UJNfGpJhatI/AAAAAAAABJs/KUnD8t2v4SU/s1600/CropperCapture%5B94%5D.jpg)

  
If you chose a type you get to see its instances

[![](images/CropperCapture_5B95_5D.jpg)](http://2.bp.blogspot.com/-aXY4gg_CrQw/UJNfHkX0dTI/AAAAAAAABJ0/bFSl09IzRk8/s1600/CropperCapture%5B95%5D.jpg)

  
Here is what is happening under the hood (i.e. the cdb.exe output)

[![](images/CropperCapture_5B96_5D.jpg)](http://3.bp.blogspot.com/-XMs6gu3IRXg/UJNfIrGU_PI/AAAAAAAABJ8/gAeiVEut_vg/s1600/CropperCapture%5B96%5D.jpg)

  
Type !help (in the textbox at the bottom) to see the list of available commands:

[![](images/CropperCapture_5B97_5D.jpg)](http://1.bp.blogspot.com/-mwGzaoFlrHo/UJNfJoSsFfI/AAAAAAAABKE/g0DozAIroAY/s1600/CropperCapture%5B97%5D.jpg)

  
Settings page with links to download the latest version of Cdb/WinDbg

[![](images/CropperCapture_5B98_5D.jpg)](http://4.bp.blogspot.com/-oV2Lz9oGJvI/UJNfKX-AwjI/AAAAAAAABKM/oVjPsAQhbkg/s1600/CropperCapture%5B98%5D.jpg)

**  
**

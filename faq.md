#FAQ - Frequently Asked Questions

##Problems Running Caleydo

**Q:** *Caleydo doesn't start, doesn't load my data, or fails somehow else. What can I do?*
**A:** Send us an e-mail with the latest log file to caleydo at icg.tugraz.at and, if possible, your dataset you tried to use. You can find your log file in the *.caleydo_2.0/logs* folder which is stored in your home directory (e.g. *C:\users\USERNAME\.caleydo\_2.0* on Windows).

**Q:** *Caleydo fails to start after updating to a new version.*
**A:** Try deleting the caches of the old version by removing *.eclipse* and *.caleydo\_2.0* folders from your home directory (e.g. *C:\users\USERNAME\.eclipse* and *C:\users\USERNAME\.caleydo\_2.0*)

**Q:** *Caleydo dose not start with the error message on the console:*

    !SESSION 2013-05-06 17:22:06.045 -----------------------------------------------
    eclipse.buildId=unknown
    java.version=1.7.0_21
    java.vendor=Oracle Corporation
    BootLoader constants: OS=macosx, ARCH=x86_64, WS=cocoa, NL=en_US
    
    !ENTRY org.eclipse.equinox.ds 4 0 2013-05-06 17:22:09.266
    !MESSAGE [SCR] Exception while activating instance org.eclipse.e4.ui.css.swt.internal.theme.ThemeEngineManager@3c867009 of component 
    org.eclipse.e4.ui.css.swt.theme  
    !STACK 0
    java.lang.NoClassDefFoundError: org/eclipse/swt/widgets/Display
           at java.lang.Class.getDeclaredMethods0(Native Method)
           at java.lang.Class.privateGetDeclaredMethods(Class.java:2451)

**A:** This error occurs when running Caleydo with the wrong system architecture, meaning that you are, for example, trying to run a 32 bit version on a 64 bit computer.

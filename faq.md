#FAQ - Frequently Asked Questions

**Q: I found a bug! What should I do?**

- Please file a bug at [github](https://github.com/Caleydo/caleydo/issues), be as clear as you can about your situation and include a the log.

**Q:** **Where do I find the logs?**

- You can find your log file in the *.caleydo_3.0/logs* folder which is stored in your home directory (e.g. *C:\Users\USERNAME\.caleydo_3.0* on Windows).

##Problems Running Caleydo

**Q:** **Caleydo fails to start after updating to a new version.**

- Try deleting the caches of the old version by removing *.eclipse* and *.caleydo\_3.0* folders from your home directory (e.g. *C:\users\USERNAME\.eclipse* and *C:\users\USERNAME\.caleydo\_3.0*)

**Q:** **Caleydo fails to start with the message: Failed to create Java Virtual Machine.**

- It seems that your machine has not enough main memory. However, you can try to reduce the initial Java Virtual Machine memory impact by manipulating the *Caleydo.ini* file. Reduce the two entries: *-Xms512m* and *-Xmx2048m* by a factor of two and try it again.

**Q:** **Caleydo does not start with the following error message on the console:**

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

- This error occurs when running Caleydo with the wrong system architecture, meaning that you are, for example, trying to run a 32 bit version on a 64 bit computer.

**Q:** **Caleydo still doesn't start, doesn't load my data, or fails somehow else. What can I do?**

- Please [file a bug](https://github.com/Caleydo/caleydo/issues) or send us an e-mail (caleydo at icg dot tugraz dot at) with the latest log file and, if possible, the dataset you tried to use. 

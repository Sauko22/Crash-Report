# Crash Reports


I am Pol Juan Santos, student of the <a href="https://www.citm.upc.edu/ing/estudis/graus-videojocs/">Bachelor’s Degree in 
Video Games by UPC at CITM</a>. This content is generated for the second year’s subject Project 2, under supervision of lecturer
<a href="https://www.linkedin.com/in/mgarrigo/">Marc Garrigó</a>.
  
## Index

<a href="#intro"><b> 1. What is a Crash? </b></a>

<a href="#crashre"><b> 2. What is Crash Reporting? </b></a>

<a href="#crashdump"><b> 3. Crash dump and Minidump files </b></a>

<a href="#visual"><b> 4. How to create a dump file in Visual Studio? </b></a>

<a href="#make"><b> 5. How to make our own Crash reporter? </b></a>

<a href="#biblio"><b> 6. Bibliography </b></a>

<h2 id="intro"> What is a Crash? </h2>
We call crash when a computer program such as a videogame, app or any kind fo software stops functioning as normal and exits. This is because the application performs an operation that is not allowed to do. Then, the operating system shuts down the program and  triggers a exception or signal indicating what was the reason the crash was produced. Typical causes include incorrect address values in the couter of the program, buffer overflow, accessing invalid memory addresses or attempting to execute machine instructions with bad arguments.
In order to fix a crash, the code must be debugged, which is the process of finding and fixing the faulty code which caused the crash so the program can run smoothly again. Then, we should report the crash to get it fixed by the company.

<img src="https://media1.tenor.com/images/86031337405fc540c2b56af57206ff6c/tenor.gif?itemid=8556865" width ="700" height="540">

<h3> Crash to deskop </h3>
A crash to deskop occurs when a program(usually videogames) unexpectedly quits,abruptly taking the user back to the deskop. Most of the time, an exception is no displayed , leaving the user without knowing what was the problem. Many times there is no apparent action that causes a crash to desktop. During normal function, the program may freeze for a shorter period of time, and then close by itself, or it may appear to be triggered by a certain action, such as loading an area. 

<img src="https://github.com/Sauko22/Crash-Report/blob/master/web/loading.jpg?raw=true">

<h3>Example</h3>
<img src="https://www.bugsplat.com/images/graphics/league_of_legends_crash_box.png" width ="200" height="260">
<i>* League of Legends </i>
<img src="https://www.mystgraphics.com/OverwatchForumImages/OverwatchCrashDialog.jpg" width ="300" height="260">
<i>* Overwatch </i>

<h2 id="crashre">What is Crash Reporting? </h2>
Is a system software whose main function is to identify reporting crash details and to alert when there are crashes.In them we can find data about he problem such as stack traces, type of crash version of the sofware we are using and general system info. These reports help sofware developers(webs,videogames,apps) to seek and fix the underlying problem causing the crashes. They may also contain sensitive information such as email addreses, users names and passwords, and so have become objects of priority security in the field of computer security.
<img src="https://media.minecraftforum.net/attachments/190/524/635939770564555905.png?raw=true">
<i>* Minecraft crash reporter </i>

Implementing crash reporting tools as very a important part of the development cycle has become an obligation,thanks to the commodity that gives. Not only for issues dicovery, but making your workflow easier. That's the case of <b>Sentry</b>, an open-source company, providing an application monitoring platform that helps you identify issues in real-time.Very used in Unreal and an excellent tool. 

<img src="https://nextcloud.com/media/sentry-logo-black-1.png?raw=true">

<h3>Sentry</h3>
<b>But,how it works? Let's see an example:</b>
There’s a bug — let’s say it’s a NullPointerException — that users start hitting post-deployment. Sentry picks up the error immediately and alerts you (or whoever is on-call) via Slack, PagerDuty, or one of many other integrations based on your notification rules.

This notification takes you to a dashboard that gives you the necessary context to quickly triage the problem — frequency, user impact, which part of the code is affected, and which team member is a likely owner for the issue (just like Github issues). Then it shows you detailed information to help you debug, like the stack trace, stack locals, preceding events, commits that likely caused the issue, type of the exception and custom data captured at the time of the error. You can also automatically start tracking the issue in your project management tool.
After identifying the problem you commit a fix to the repository. At this point, you no longer need to  on alert  about the fix because Sentry watches commits as they go in and automatically resolves the issue when it gets deployed. If the issue returns later, it’s marked as a regression and you’re notified again.

Meanwhile, the user who encountered the error didn’t even need to send you a message to help you fix the bug. Notably, though, Sentry can also offer those users a friendly way to send additional information that might help you resolve the issue even faster.

<img src="https://sentry.io/_assets/screenshots/features-page-dash-12c65431808e7d8daf234a096446c1f0da311a0f3bcec5352e28bda60136fb16.jpg?raw=true">

<h2 id="crashdump"> Crash dump and Minidump files </h2>
However, let's get back on crash reporting. We could compare a crash report as a Blacbox, and its application as an airplane.
<img src="https://cdn-images-1.medium.com/max/1200/1*WljD7gLyX2gr_60o501Z1A.png" width ="200" height="200">

Blackbox records all vital information so when the application crash, you can easily find the reason, in this case:
<ul>
  <li>Error type</li>
  <li>Callstack</li>
  <li>Register Contents</li>
  <li>General system info(CPU,memory,OS,etc)</li>
 </ul>
Messages aren’t displayed anywhere, so users aren’t bothered, they don’t even know it’s happening. What to record? Well, it’s up to you. In our case, name of loaded resource, would surely be a good bet. This way, on crash all you have to do is to check latest blackbox messages (for thread that crashed). But, what are these blackbox messages? Well, would be talking about <b>Crash Dump and Mini Dump files</b>. 

<h3>Crash Dumps</h3>
Crash dump or memory dump consists of the recorde state of the working memory of a program at a specific time, generally when that one has crashed.In practice, are used to assist in diagnosing and debbugging errors. Other key pieces of program state are usually dumped at the same time, including the processor registers, which may include the program counter and stack pointer, memory management information, and other processor and operating system flags and information. A snapshot dump is a memory dump requested by the computer operator or by the running program, after which the program is able to continue.

<img src="https://www.drivethelife.com/uploadfiles/20180807/error-fix-blue-screen-memory-dump.png?raw=true">

<h3>MiniDumps</h3>
Minidumps are files containing the most important memory regions of a crashed process. When the process crashes, the minidump is written to the user’s disk. A minidump typically includes:

  <ul>
  <li>The runtime stack of each thread that was active during the time of the crash. This allows yout to reconstruct stack traces for all stacks and even infer variable values in some cases.</li>
  <li>Thread contexts – that is, register values – at the time of the crash. This is especially relevant for stack walking.</li>
  <li>The crash reason and an optional memory address associated to with the crash. For example, memory access violations. In the case of assertions, the assertion message is also included in the dump.</li>
  <li>Meta data about the CPU architecture and the user’s operating system.</li>
 </ul>
 
MiniDump files may or may not have heap information.
 <ul>
  <li><b>Dump files with heaps</b> contain a snapshot of the app's memory, including the values of variables, at the time of the dump.
  </li>
  <li><b>Dump files without heaps</b> are much smaller than dumps with heaps, but the debugger must load the app binaries to find symbol information. The loaded binaries must exactly match the ones running during dump creation. Dump files without heaps save the values of stack variables only.</li>
  </ul>
  <img src="https://www.codeproject.com/KB/applications/minidump/MiniDump.gif?raw=true">

<h2 id="visual">How to create a dump file in Visual Studio? </h2>
Now that we what dump files are used for, let's used them on visual studio.
While you are debugging a process in Visual Studio, you can save a dump when the debugger has stopped at an exception or breakpoint.
Before we start, you need to have Just-In-Time Debbugging enable,that allow you to attach the Visual Studio debugger to a crashed process outside of Visual Studio, and then save a dump file from the debugger. <a href="https://docs.microsoft.com/en-us/visualstudio/debugger/attach-to-running-processes-with-the-visual-studio-debugger?view=vs-2019"> Attach to running processes</a>

<h3>To save a dump file</h3>
<ul>
  <li>While stopped at an error or breakpoint during debugging, select <b> Debug > Save Dump As</b>.
  </li>
  <li>In the Save Dump As dialog box, under Save as type, select Minidump or Minidump with Heap (the default).</li>
  <li>Browse to a path and select a name for the dump file, and then select Save.</li>
  </ul>
<img src="https://github.com/Sauko22/Crash-Report/blob/master/web/dumpfile.png?raw=true?raw=true">
  
<h3>Open a dump file</h3>
<ul>
  <li>In Visual Studio, select <b>File > Open > File</b>.
  </li>
  <li>In the Open File dialog box, locate and select the dump file. It will usually have a .dmp extension. Select OK.</li>
  </ul>
The Minidump File Summary window shows summary and module information for the dump file, and actions you can take.
<img src="https://i.stack.imgur.com/LfZFh.jpg?raw=true?raw=true">
If you press <b>debug Native Only</b>, it will send you to where the problem or the breakpoint produced the crash.
  
<h2 id="make">How to make our own Crash reporter? </h2>
So ,there you have it. You now know all the basic abot crash report, and how to use it in visual studio. But, can we make a crash reporter for our own videogame? Well, it is posible to do it.
Down below you can read an article done by a programmer from The Witcher, explaining how was his experience proggramming one, talking about what we just saw but in action and giving some advices about the topic. 

<img src="https://i.imgur.com/TOtVqjm.png?raw=true">
<a href="http://msinilo.pl/blog2/post/p269/"> Crash handler/reporter (Win32) by Maciej Sinilo</a>

<h2 id="biblio">Bibliography</h2>

+ <a href="https://docs.sentry.io/"> Sentry Web Page</a>
+ <a href="https://en.wikipedia.org/wiki/Core_dump#MINIDUMP"> Wikipedia-Core Dump</a>
+ <a href="https://techcommunity.microsoft.com/t5/ask-the-performance-team/understanding-crash-dump-files/ba-p/372633#"> Understanding Crash Dumps Files</a>
+ <a href="https://docs.microsoft.com/en-us/windows/win32/debug/minidump-files"> MiniDumps Files</a>
+ <a href="http://msinilo.pl/blog2/post/p269/"> Crash handler/reporter (Win32) by Maciej Sinilo</a>
+ <a href="https://docs.microsoft.com/en-us/windows/win32/dxtecharts/crash-dump-analysis"> Crash Dump Analysis</a>





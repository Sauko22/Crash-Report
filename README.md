# Crash Reports


I am Pol Juan Santos, student of the <a href="https://www.citm.upc.edu/ing/estudis/graus-videojocs/">Bachelor’s Degree in 
Video Games by UPC at CITM</a>. This content is generated for the second year’s subject Project 2, under supervision of lecturer
<a href="https://www.linkedin.com/in/mgarrigo/">Marc Garrigó</a>.
  

<h2 id="intro"> What is a Crash? </h2>
We call crash when a computer program such as a videogame, app or any kind fo software stops functioning as normal and exits. This is because the application performs an operation that is not allowed to do. Then, the operating system shuts down the program and  triggers a exception or signal indicating what was the reason the crash was produced. Typical causes include incorrect address values in the couter of the program, buffer overflow, accessing invalid memory addresses or attempting to execute machine instructions with bad arguments.
In order to fix a crash, the code must be debugged, which is the process of finding and fixing the faulty code which caused the crash so the program can run smoothly again. Then, we should report the crash to get it fixed by the company.

<img src="https://github.com/Sauko22/Crash-Report/blob/master/web/blue%20screen.png?raw=true">

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



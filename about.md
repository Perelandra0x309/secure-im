---
layout: single
title: About This Site
---
Welcome to my website about secure messaging apps for Android, iOS and desktops!<br>
<br>
I started this site as a way for me to just keep track of all the information I was gathering about different features of apps I was hearing about.  I sometimes would give my site as a reference when I was asked a question about a certain app, and many people found the site useful so I decided to keep going and adding more features over time.  I will try to keep the information up to date and add new apps that I think are worthy of reviewing.<br>
<br>
I am by no means an expert in cryptography, it is a very complicated subject and I am learning as best I can as I research these apps.  If you do find a mistake, or wish to make a suggestion please head on over to my github repo and <a target="_blank" href="https://github.com/Perelandra0x309/secure-im/issues">create an issue ticket there</a>.  I also add issues there to remind myself of things to add or investigate.<br>
<br>
<h3 id="testing">My testing setup:</h3>
I test on iOS, Android, MacOS and web applications.  Keep in mind that even though you may be using one platform, the other person you are communicating with may be using a different platform.  iOS is generally more secure than Android, simply because the application data is very well segregated at the OS level, so that apps cannot access the data of other apps.  However this is not the case with Android, each application written for Android must ensure it does not save any data to globally accessible local storage.  So when I test apps I scrutinize the Android version very closely to look for any data leakage. So even if an iOS version of an app does not leak data, if the Android version does I consider the entire app system compromised.<br>
<br id="testsetup">
My test devices:
<ul>
  <li>Motorola G4 Plus with stock Android 8.1</li>
  <li>iPhone 5S with iOS 12.4.6</li>
</ul>
For apps that require a phone number I use two VOIP numbers that have SMS capability so I don't expose my primary phone number.  One is through the MySudo app on iOS, and the other is through <a target="_blank" href="https://jmp.chat">JMP.chat</a>.  These are only available in the US/Canada.<br>
<br>
<h3>About this website:</h3>
Since this is a website about security and privacy I will try to keep all use of external third party resources to the minimum necessary.  I will self host as many files on this server as possible to avoid your web browser making unnecessary requests to other servers.  There are some things on this site which do require javascript, however these features are optional and only enable some functionality like filtering in the large tables on the Features Matrix and Practical Application of the EFF Guide pages.<br>
<br>
Changes to this website can be tracked using <a href="https://github.com/perelandra0x309/secure-im/commits/master.atom">this Atom feed</a>.

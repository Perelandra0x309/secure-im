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
<p id="testing">My testing setup:</p>
I test on iOS, Android, MacOS and web applications.  Keep in mind that even though you may be using one platform, the other person you are communicating with may be using a different platform.  iOS is generally more secure than Android, simply because the application data is very well segregated at the OS level, so that apps cannot access the data of other apps.  However this is not the case with Android, each application written for Android must ensure it does not save any data to globally accessible local storage.  So when I test apps I scrutinize the Android version very closely to look for any data leakage. So even if an iOS version of an app does not leak data, if the Android version does I consider the entire app system compromised.<br>
<br>
My test devices:
<ul>
  <li>Motorola G4 Play with stock Android 7.1.1</li>
  <li>iPhone 5S with iOS 12.1</li>
</ul>
For apps that require a phone number I use two VOIP numbers that have SMS capability so I don't expose my primary phone number.  One is through the MySudo app on iOS, and the other is through <a target="_blank" href="https://jmp.chat">JMP.chat</a>.  These are only available in the US/Canada.<br>

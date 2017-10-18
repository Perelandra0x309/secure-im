# secure-im
My list of secure messaging apps.  Below are applications that offer end to end encryption.<br>
For now just a list of my notes.  May cleanup later.<br>

<p>Apps rejected because they are not E2EE:
<ul>
<li>Facebook Messenger</li>
<li>Google Hangouts</li>
<li>Riot (well E2EE still beta)</li>
<li>Skype</li>
<li>Trello</li>
</ul>
<p>
<p>To investigate:
<ul>
<li>Mumble</li>
<li>Jitsi</li>
<li>Slack</li>
<li>Semaphor (maybe?)</li>
<li>OnionShare</li>
<li>WhatsApp</li>
</ul>

<table>
  <tr><td colspan="4"><b>P2P Serverless Open Source</b></td></tr>
  <tr><td><b>Application (notes)</b></td>
  <td><b>Platforms</b></td>
  <td><b>Communication types</b></td>
  <td><b>Websites</b></td></tr>

<tr>
  <td><a href="https://briarproject.org">Briar Project</a></td>
  <td>Android (doesn't need play services) via Google Play, <a href="https://briarproject.org/fdroid.html">F-Droid repo</a> or <a href="https://briarproject.org/apk.html">APK</a></td>
  <td>Text and forums</td>
  <td><a href="https://code.briarproject.org/akwizgran/briar/tree/master">Source Code</a></td>
</tr>
<tr><td colspan="4">
    Pros:<br>
    Secure P2P encryption<br>
    On F-Droid<br>
    Does not require Google Play services<br>
    Works over <a href="https://briarproject.org/how-it-works.html">wifi, bluetooth or Tor</a><br>
    Cons:<br>
    Android only<br>
    Pro or Con:<br>
    Requires physical presence of contacts for initial verification (by design)  
</td></tr>

<tr>
  <td><a href="https://ricochet.im">Ricochet</a></td>
  <td><a href="https://ricochet.im/releases/latest/">Windows, Mac, Linux</a></td>
  <td>Text</td>
  <td><a href="https://github.com/ricochet-im/ricochet">Source Code</a></td>
</tr>
<tr><td colspan="4">
    Works over Tor<br>
    Is this still in active development??
</td></tr>

<tr>
  <td><a href="https://ring.cx">Ring</a></td>
  <td><a href="https://ring.cx/en/download">Android, Linux, Mac, Windows (soon iOS)</a></td>
  <td>Text, voice, video</td>
  <td><a href="https://github.com/savoirfairelinux/">Source Code</a></td>
</tr>
<tr><td colspan="4">
    Pros:<br>
    On F-Droid<br>
    Multiple platforms<br>
    Not dependent on a phone #<br>
    Cons:<br>
    Android and Mac app still have usability issues, just out of beta
</td></tr>

<tr>
  <td><a href="https://tox.chat">Tox</a></td>
  <td><a href="https://tox.chat/download.html">Windows, Mac, Linux, FreeBSD, iOS, Android</a></td>
  <td>Text, voice, video, screen sharing, file sharing</td>
  <td><a href="https://github.com/TokTok/c-toxcore">toxcore source</a></td>
</tr>
<tr><td colspan="4">
  toxcore was <a href="https://tox.chat/download.html#toktok-c-toxcore">forked</a> to continue development<br>
  <br>
  What is leaked to the world:[1]<br>
- Your IP address and the time you are online is revealed to your contacts. When chatting to another contact, you are connecting directly to them.<br>
- Tor activity for contact finding.<br>
- Not sure what else? There may be more. Going to have to read the documentation.
  </td></tr>

<tr><td colspan="4"><b>Federated and Centralized Open Source</b></td></tr>
  <tr><td><b>Application (notes)</b></td>
  <td><b>Platforms</b></td>
  <td><b>Communication types</b></td>
  <td><b>Websites</b></td></tr>

<tr>
  <td>XMPP (with <a href="https://wiki.xmpp.org/web/OTR">OTR</a> or OMEMO)</td>
  <td>Linux, Windows, MacOS, Android, iOS</td>
  <td></td>
  <td><a href="https://xmpp.org">xmpp.org</a></td>
</tr>
<tr><td colspan="4">
<a href="https://otr.cypherpunks.ca/software.php">OTR clients</a><br>
OMEMO Clients:<br>
<ul>
<li>Android- <a href="https://conversations.im/">Conversations</a>
<li>iOS- <a href="https://chatsecure.org/">ChatSecure</a>
<li>Linux and Windows- <a href="https://gajim.org/">Gajim</a> with <a href="https://dev.gajim.org/gajim/gajim-plugins/wikis/OmemoGajimPlugin">OmemoGajimPlugin</a>
<li>Linux- <a href="https://www.pidgin.im/">Pidgin</a> with <a href="https://github.com/gkdr/lurch">lurch</a>
<li>MacOS- <a href="https://adium.im/">Adium</a> with <a href="https://github.com/shtrom/Lurch4Adium">Lurch4Adium</a>
</ul>
<br>
  What the server sees:[1]<br>
- Your plaintext chats unless you use encryption such as OTR, PGP, or OMEMO.<br>
- Your contact list is saved to the server in plaintext<br>
- Precise time you logged in or out<br>
- Precise time you sent any messages to a contact and what messages they send you.<br>
- Whether you are online or not, and your status.<br>
- Who you contacted, when, and how frequently.<br>
- SHA-1 hash of your password. Improperly configured servers may store passwords in plaintext.
  </td></tr>

<tr>
  <td><a href="https://trac.torproject.org/projects/tor/wiki/doc/TorMessenger">Tor Messenger</a></td>
  <td></td>
  <td></td>
  <td></td>
</tr>

<tr>
  <td><a href="http://www.kontalk.org">Kontalk (XMPP)</a></td>
  <td><a href="https://github.com/kontalk/androidclient/releases">Android</a> (does not require Google Play), <a href="https://github.com/kontalk/desktopclient-java/releases">Java</a></td>
  <td>text</td>
  <td><a href="https://github.com/kontalk/desktopclient-java">Java Client source</a>,<br>
    <a href="https://github.com/kontalk/androidclient">Android client source</a></td>
</tr>
<tr><td colspan="4">
  Pros:<br>
    On F-Droid<br>
    Not dependent on Google play services<br>
  Cons:<br>
    People have to know your phone#
 </td></tr>

<tr>
  <td><a href="https://www.signal.org">Signal</a></td>
  <td>Android (<a href="https://signal.org/android/apk/">Direct APK download</a>), iPhone, Desktop</td>
  <td></td>
  <td></td>
</tr>
<tr><td colspan="4">
  What the server sees:[1]<br>
- The phone number used for your registration.<br>
- SHA-2 Hashes of your contacts' telephone numbers to check for a match. OWS claims to delete this as soon as it is no longer needed.
  What Signal claims to keep:<br>
- The day you first joined the service<br>
- The last day you used it.<br>
Disadvantages:<br>
- People must know your phone number. It is possible to register a burner number or a VOIP number, but this is an advanced-use case.
</td></tr>

<tr>
  <td><a href="https://www.keybase.io">Keybase</a></td>
  <td></td>
  <td></td>
  <td></td>
</tr>

<tr>
  <td><a href="http://retroshare.net">RetroShare</a></td>
  <td><a href="http://retroshare.net/downloads.html">Windows, Mac, Linux</a></td>
  <td>Text, voice, video, email, file sharing</td>
  <td><a href="https://github.com/RetroShare/RetroShare">Source code</a></td>
</tr>

<tr><td colspan="4"><b>P2P Serverless Closed Source</b></td></tr>
  <tr><td><b>Application (notes)</b></td>
  <td><b>Platforms</b></td>
  <td><b>Communication types</b></td>
  <td><b>Websites</b></td></tr>

<tr>
  <td><a href="https://twin.me">TwinMe</a></td>
  <td>Android, iOS</td>
  <td>Text, voice, video</td>
  <td><a href="https://twin.me/en/support/twinme-protect-data/">Encryption</a></td>
</tr>

<tr><td colspan="4"><p align="center"><b>Federated or Centralized Closed Source</b></p></td></tr>
  <tr><td><b>Application (notes)</b></td>
  <td><b>Platforms</b></td>
  <td><b>Communication types</b></td>
  <td><b>Websites</b></td></tr>

<tr>
  <td><a href="https://www.wickr.com">Wickr</a></td>
  <td></td>
  <td></td>
  <td></td>
</tr>

<tr>
  <td><a href="https://wire.com">Wire</a></td>
  <td></td>
  <td></td>
  <td></td>
</tr>
<tr><td colspan="4">
What the server sees and may save:[1]<br>
- Your contact list is saved to the server in plaintext.<br>
- Who you talk to, when, and for how long.  
</td></tr>

<tr>
  <td><a href="https://threema.ch">Threema</a></td>
  <td></td>
  <td></td>
  <td></td>
</tr>

<tr>
  <td><a href="https://telegram.org">Telegram</a> (E2EE only in secret chats)</td>
  <td></td>
  <td></td>
  <td></td>
</tr>
<tr><td colspan="4">
  Metadata leakage:[1]<br>
- When you are online or not or whether the application is running or not is publicly viewable.<br>
- Who you talk to, when, and the precise time you send a message, and how frequently is publicly viewable via commandline tools.<br>
- If an attacker knows your phone number, the attacker will be able to silently log your Telegram activity without you knowing about it or being informed they have you as a contact.<br>
  Stalking via Telegram through the use of Commandline Tools (Flisback, Ola, updated 2015, December 16th)<br>
<a href="https://oflisback.github.io/telegram-stalking/">https://oflisback.github.io/telegram-stalking/</a><br>

Contact Theft through Telegram, Paragraph 9 and 10.<br>
"Operational Telegram"  "The Grugq (assumed name" (Posted November 18th, 2015)<br>
<a href="https://medium.com/@thegrugq/operational-telegram-cbbaadb9013a#.a62knhv8x">https://medium.com/@thegrugq/operational-telegram-cbbaadb9013a#.a62knhv8x</a><br>

A practical Analysis of the Telegram Messaging Protocol<br>
Jakobsen, Jakob B. (Published September 2015)<br>
<a href="http://cs.au.dk/~jakjak/master-thesis.pdf">http://cs.au.dk/~jakjak/master-thesis.pdf</a>
  </td></tr>

</table>

<br>
<br>
Other similar resources:<br>
<a href="https://www.privacytools.io/#im">privacytools.io</a><br>
<a href="https://prism-break.org">Prism Break</a><br>
<a href="https://ssd.eff.org/en/module/communicating-others">EFF- Communication with Others</a><br>
<a href="https://hackernoon.com/encrypted-instant-messaging-recommendations-january-2017-711c03af02cc">Marcel Ackermann's recommendations</a><br>
<a href="https://yawnbox.com/2017/05/01/secure-messenger-scorecard-may-2017/">yawnbox's Secure Messagenger Scorecard</a><br>

<br>
Sources:
<pre>[1]: Information provided by JR</pre>

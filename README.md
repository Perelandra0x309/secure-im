# secure-im
My list of secure messaging apps.  Below are applications that offer end to end encryption.<br>
For now just a list of my notes.  May cleanup later.<br>

<table>
  <tr><td colspan="4"><p align="center"><b>P2P Serverless Open Source</b></p></td></tr>
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
    <li>Pros:</li>
    Secure P2P encryption<br>
    On F-Droid<br>
    Does not require Google Play services<br>
    Works over <a href="https://briarproject.org/how-it-works.html">wifi, bluetooth or Tor</a><br>
    <li>Cons:</li>
    Android only<br>
    <li>Pro or Con:</li>
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
    <li>Pros:</li>
    On F-Droid<br>
    Multiple platforms<br>
    Not dependent on a phone #<br>
    <li>Cons:</li>
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

<tr><td colspan="4"><p align="center"><b>Federated and Centralized Open Source</b></p></td></tr>
  <tr><td><b>Application (notes)</b></td>
  <td><b>Platforms</b></td>
  <td><b>Communication types</b></td>
  <td><b>Websites</b></td></tr>

<tr>
  <td>XMPP (with OTR or OMEMO)</td>
</tr>
<tr><td colspan="4">
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
</tr>

<tr>
  <td><a href="http://www.kontalk.org">Kontalk (XMPP)</a></td>
  <td><a href="https://github.com/kontalk/androidclient/releases">Android</a> (does not require Google Play), <a href="https://github.com/kontalk/desktopclient-java/releases">Java</a></td>
  <td>text</td>
  <td><a href="https://github.com/kontalk/desktopclient-java">Java Client source</a>,<br>
    <a href="https://github.com/kontalk/androidclient">Android client source</a></td>
</tr>
<tr><td colspan="4">
  <li>Pros:</li>
    On F-Droid<br>
    Not dependent on Google play services<br>
  <li>Cons:</li>
    People have to know your phone#
 </td></tr>

<tr>
  <td><a href="https://www.signal.org">Signal</a></td>
  <td></td>
  <td>Android (<a href="https://signal.org/android/apk/">Direct APK download</a>), iPhone, Desktop</td>
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
</tr>

<tr>
  <td><a href="http://retroshare.net">RetroShare</a></td>
  <td><a href="http://retroshare.net/downloads.html">Windows, Mac, Linux</a></td>
  <td>Text, voice, video, email, file sharing</td>
  <td><a href="https://github.com/RetroShare/RetroShare">Source code</a></td>
</tr>

<tr><td colspan="4"><p align="center"><b>P2P Serverless Closed Source</b></p></td></tr>
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
  <td>Wickr</td>
</tr>

<tr>
  <td>Wire</td>
</tr>
<tr><td colspan="4">
What the server sees and may save:[1]<br>
- Your contact list is saved to the server in plaintext.<br>
- Who you talk to, when, and for how long.  
</td></tr>

<tr>
  <td>Threema</td>
</tr>

<tr>
  <td>Telegram (E2EE only in secret chats)</td>
</tr>
<tr><td colspan="4">
  Metadata leakage:[1]<br>
- When you are online or not or whether the application is running or not is publicly viewable.<br>
- Who you talk to, when, and the precise time you send a message, and how frequently is publicly viewable via commandline tools.<br>
- If an attacker knows your phone number, the attacker will be able to silently log your Telegram activity without you knowing about it or being informed they have you as a contact.<br>
  Stalking via Telegram through the use of Commandline Tools (Flisback, Ola, updated 2015, December 16th)<br>
https://oflisback.github.io/telegram-stalking/<br>

Contact Theft through Telegram, Paragraph 9 and 10.<br>
"Operational Telegram"  "The Grugq (assumed name" (Posted November 18th, 2015)<br>
https://medium.com/@thegrugq/operational-telegram-cbbaadb9013a#.a62knhv8x<br>

A practical Analysis of the Telegram Messaging Protocol<br>
Jakobsen, Jakob B. (Published September 2015)<br>
http://cs.au.dk/~jakjak/master-thesis.pdf
  </td></tr>

</table>

Sources:
<pre>[1]: Information provided by JR</pre>

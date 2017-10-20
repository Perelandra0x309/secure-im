# secure-im
My list of secure messaging apps.  Below are applications that offer end to end encryption.<br>
For now just a list of my notes.  May cleanup later.<br>
In the table I break up the apps into four groups, split by whether they are open source or not, and whether they are strict Peer-to-Peer or require some type of federated or centralized infrastructure.  This may help to narrow down your search if you are only looking for open source, or only Peer-to-Peer for example.<br>
Corrections and additions are welcome, either by an Issue ticket or a Pull Request on the <a href="https://github.com/Perelandra0x309/secure-im">github project page</a>.<br>

<h3>My current top picks:</h3><br>
P2P:<br>
Ring, because it is multiple platform<br>
Runners up:<br>
Ricochet<br>
Briar, when you can meet in person<br>
<br>
Federated or Centralized:<br>
XMPP with OMEMO, because of encrypted group chats and multiple clients<br>
Runners up:<br>
Riot/Matrix<br>
Keybase.io<br>


<table>
  <tr><td colspan="4" style="text-align:center"><H2>P2P Serverless Open Source</H2></td></tr>
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
    Is this still in active development??<br>
    Creates a <a href="https://www.torproject.org/docs/hidden-services.html.en">hidden Tor service</a> to connect P2P.
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
<pre>  What is leaked to the world:[1]<br>
- Your IP address and the time you are online is revealed to your contacts. When chatting to another contact,
  you are connecting directly to them.<br>
- Tor activity for contact finding.<br>
- Not sure what else? There may be more. Going to have to read the documentation.</pre>
  </td></tr>

<tr><td colspan="4" style="text-align:center"><H2>Federated and Centralized Open Source</H2></td></tr>
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
  <li>Android- <a href="https://conversations.im/">Conversations</a></li>
  <li>iOS- <a href="https://chatsecure.org/">ChatSecure</a></li>
  <li>Linux and Windows- <a href="https://gajim.org/">Gajim</a> with <a href="https://dev.gajim.org/gajim/gajim-plugins/wikis/OmemoGajimPlugin">OmemoGajimPlugin</a></li>
  <li>Linux- <a href="https://www.pidgin.im/">Pidgin</a> with <a href="https://github.com/gkdr/lurch">lurch</a></li>
  <li>MacOS- <a href="https://adium.im/">Adium</a> with <a href="https://github.com/shtrom/Lurch4Adium">Lurch4Adium</a></li>
</ul>
<br>
<pre>  What the server sees:[1]<br>
- Your plaintext chats unless you use encryption such as OTR, PGP, or OMEMO.<br>
- Your contact list is saved to the server in plaintext<br>
- Precise time you logged in or out<br>
- Precise time you sent any messages to a contact and what messages they send you.<br>
- Whether you are online or not, and your status.<br>
- Who you contacted, when, and how frequently.<br>
- SHA-1 hash of your password. Improperly configured servers may store passwords in plaintext.<br></pre>
</td></tr>

<tr>
  <td><a href="https://trac.torproject.org/projects/tor/wiki/doc/TorMessenger">Tor Messenger</a></td>
  <td>Linux, Windows, MacOS</td>
  <td>Text</td>
  <td></td>
</tr>
<tr><td colspan="4">
Connect via multiple OTR protocols (IRC, XMPP, Google Talk, etc.)
**Please note that Tor Messenger is still in beta.**
</td></tr>

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
<pre>  What the server sees:[1]<br>
- The phone number used for your registration.<br>
- SHA-2 Hashes of your contacts' telephone numbers to check for a match. OWS claims to delete this as soon as it
  is no longer needed.
  What Signal claims to keep:<br>
- The day you first joined the service<br>
- The last day you used it.<br>
Disadvantages:<br>
- People must know your phone number. It is possible to register a burner number or a VOIP number, but this is an
  advanced-use case.</pre>
</td></tr>

<tr>
  <td><a href="https://www.keybase.io">Keybase.io</a></td>
  <td><a href="https://keybase.io/download">Android, iOS, MacOS, Windows, Linux</a></td>
  <td>Text, file sharing</td>
  <td><a href="https://github.com/keybase">Source code</a></td>
</tr>
<tr><td colspan="4">
  You can also verify other website identities, GPG keys, domains, etc that you own.
</td></tr>

<tr>
  <td><a href="http://retroshare.net">RetroShare</a></td>
  <td><a href="http://retroshare.net/downloads.html">Windows, Mac, Linux</a></td>
  <td>Text, voice, video, email, file sharing</td>
  <td><a href="https://github.com/RetroShare/RetroShare">Source code</a></td>
</tr>

<tr>
  <td><a href="https://about.riot.im">Riot/Matrix</a></td>
  <td><a href="https://about.riot.im/downloads/">Android, iOS, Linux, Mac, Windows, Web</a></td>
  <td>Text, voice, video, file sharing</td>
  <td><a href="https://github.com/vector-im">Source code</a></td>
</tr>
<tr><td colspan="4">
Riot <a href="https://about.riot.im/security/">Security</a> (E2EE still in beta)<br>
  The web app can be used over Tor (thanks lwinch2006)
</td></tr>

<tr><td colspan="4" style="text-align:center"><H2>P2P Serverless Closed Source</H2></td></tr>
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

<tr><td colspan="4" style="text-align:center"><H2>Federated or Centralized Closed Source</H2></td></tr>
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
<pre>What the server sees and may save:[1]<br>
- Your contact list is saved to the server in plaintext.<br>
- Who you talk to, when, and for how long.</pre>
</td></tr>

<tr>
  <td><a href="https://threema.ch">Threema</a></td>
  <td></td>
  <td></td>
  <td></td>
</tr>

<tr>
  <td><a href="https://telegram.org">Telegram</a> (E2EE only in secret chats)</td>
  <td><a href="https://telegram.org/apps">Android, iOS, Windows, MacOS, web</a></td>
  <td>Text, voice, file sharing</td>
  <td><a href="https://telegram.org/faq#q-how-secure-is-telegram">Security</a></td>
</tr>
<tr><td colspan="4">
<pre>  Metadata leakage:[1]<br>
- When you are online or not or whether the application is running or not is publicly viewable.<br>
- Who you talk to, when, and the precise time you send a message, and how frequently is publicly viewable via
  commandline tools.<br>
- If an attacker knows your phone number, the attacker will be able to silently log your Telegram activity without
  you knowing about it or being informed they have you as a contact.<br>
  Stalking via Telegram through the use of Commandline Tools (Flisback, Ola, updated 2015, December 16th)<br>
<a href="https://oflisback.github.io/telegram-stalking/">https://oflisback.github.io/telegram-stalking/</a><br>

Contact Theft through Telegram, Paragraph 9 and 10.<br>
"Operational Telegram"  "The Grugq (assumed name" (Posted November 18th, 2015)<br>
<a href="https://medium.com/@thegrugq/operational-telegram-cbbaadb9013a#.a62knhv8x">https://medium.com/@thegrugq/operational-telegram-cbbaadb9013a#.a62knhv8x</a><br>

A practical Analysis of the Telegram Messaging Protocol<br>
Jakobsen, Jakob B. (Published September 2015)<br>
<a href="http://cs.au.dk/~jakjak/master-thesis.pdf">http://cs.au.dk/~jakjak/master-thesis.pdf</a></pre>
  </td></tr>

</table>

<p>Apps rejected because they are not E2EE:</p>
<ul>
  <li>Facebook Messenger</li>
  <li>Google Hangouts</li>
  <li>Yahoo Messenger, AIM, ICQ</li>
  <li>Skype</li>
  <li>Trello</li>
</ul>
<br>
<p>Apps rejected for other reasons:</p>
<ul>
  <li>WhatsApp- <a href="https://www.eff.org/deeplinks/2016/10/where-whatsapp-went-wrong-effs-four-biggest-security-concerns">EFF's concerns</a>:<br>
    -Unencrypted backups at rest<br>
    -Data sharing with Facebook
  </li>
</ul>
<br>
<p>To investigate:</p>
<ul>
  <li>Facetime, iMessage</li>
  <li>Surespot</li>
<li>Mumble</li>
<li>Jitsi</li>
<li>Slack</li>
<li>Semaphor (maybe?)</li>
<li>OnionShare</li>
</ul>
<br>
<br>
Other similar resources:<br>
<a href="https://www.privacytools.io/#im">privacytools.io</a><br>
<a href="https://prism-break.org">Prism Break</a><br>
<a href="https://ssd.eff.org/en/module/communicating-others">EFF- Communication with Others</a> (Also <a href="https://www.eff.org/secure-messaging-scorecard">EFF messaging scorecard</a> is out of date but still useful)<br>
<a href="https://ssd.eff.org">EFF Surveillence Self-Defense</a><br>
<a href="https://hackernoon.com/encrypted-instant-messaging-recommendations-january-2017-711c03af02cc">Marcel Ackermann's recommendations</a><br>
<a href="https://yawnbox.com/2017/05/01/secure-messenger-scorecard-may-2017/">yawnbox's Secure Messagenger Scorecard</a><br>

<br>
Sources:
<pre>[1]: Information provided by JR</pre>

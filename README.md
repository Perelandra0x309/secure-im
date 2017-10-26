# secure-im
My list of secure messaging apps.  Below are applications that offer end to end encryption.<br>
For now just a list of my notes.  May cleanup later.<br>
In the table I break up the apps into four groups, split by whether they are open source or not, and whether they are strict Peer-to-Peer or require some type of federated or centralized infrastructure.  This may help to narrow down your search if you are only looking for open source, or only Peer-to-Peer for example.<br>
Corrections and additions are welcome, either by an Issue ticket or a Pull Request on the <a href="https://github.com/Perelandra0x309/secure-im">github project page</a>.<br>

<h3>My current top picks:</h3><br>
Criteria:
<ul>
<li>This list is focused on instant messaging and chatting as the primary usage of the app</li>
<li>Open source</li>
<li>Multiple platforms preferred</li>
</ul>
The list:
<ul>
  <li>P2P:</li>
  <ul>
    <li>Ring</li>
    <li>Runners up:</li>
    <li>Ricochet</li>
  </ul>
<br>
  <li>Federated or Centralized:</li>
  <ul>
    <li>XMPP with OMEMO, because of encrypted group chats and multiple clients</li>
    <li>Runners up:</li>
    <li>Riot/Matrix</li>
    <li>Keybase.io</li>
  </ul>
</ul>
If you're not so strict about being open source try:
<ul>
  <li>Eleet</li>
  <li>Threema</li>
</ul>

<h3>Application Information:</h3>
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
  <td>Text, group chat, voice, video</td>
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
<pre>
What is leaked to the world:[1]
- Your IP address and the time you are online is revealed to your contacts. When chatting
  to another contact, you are connecting directly to them.
- Tor activity for contact finding.
- Not sure what else? There may be more. Going to have to read the documentation.
</pre>
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
<pre>
What the server sees:[1]
- Your plaintext chats unless you use encryption such as OTR, PGP, or OMEMO.
- Your contact list is saved to the server in plaintext
- Precise time you logged in or out
- Precise time you sent any messages to a contact and what messages they send you.
- Whether you are online or not, and your status.
- Who you contacted, when, and how frequently.
- SHA-1 hash of your password. Improperly configured servers may store passwords in plaintext.
</pre>
</td></tr>

<tr>
  <td><a href="https://trac.torproject.org/projects/tor/wiki/doc/TorMessenger">Tor Messenger</a></td>
  <td>Linux, Windows, MacOS</td>
  <td>Text</td>
  <td></td>
</tr>
<tr><td colspan="4">
Connect via multiple OTR protocols (IRC, XMPP, Google Talk, etc.)<br>
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
  <td>Text, voice, video, files, images</td>
  <td><a href="https://github.com/WhisperSystems">Source Code</a>, <a href="https://www.signal.org/docs/">Technical docs</a></td>
</tr>
<tr><td colspan="4">
Requires a phone number to register
<pre>
What the server sees:[1]
- The phone number used for your registration.
- SHA-2 Hashes of your contacts' telephone numbers to check for a match. OWS claims
  to delete this as soon as it is no longer needed.<br>
What Signal claims to keep:
- The day you first joined the service
- The last day you used it.<br>
Disadvantages:
- People must know your phone number. It is possible to register a burner number or
  a VOIP number, but this is an advanced-use case.
</pre>
</td></tr>

<tr>
  <td><a href="https://www.keybase.io">Keybase.io</a></td>
  <td><a href="https://keybase.io/download">Android, iOS, MacOS, Windows, Linux</a></td>
  <td>Text, group chat, file sharing</td>
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
<tr><td colspan="4">
<pre>
What is leaked to the world when using the DHT.[1]
- Your IP address.
- The IP addresses that you are connecting to.
Optionally, Retroshare may be configured to tunnel through I2P or Tor
with friend finding turned off to function as a true darknet. This
however, is slow, unreliable, high-latency, and very difficult to set up.



- Retroshare may appear to use PGP, but what actually seems to be
happening under the hood is that it's using the RSA keys to sign
ephemeral keys which are then used to establish connections to your
friends via perfect forward secrecy. The PGP parts of it look like they
are used only for certifying and authentication, and are not used to
encrypt the data.

- Certificate authorities are not used, the networks are fully
friend-to-friend. This is markedly different from peer-to-peer because
it is expected in a friend-to-friend network, you already know, and
already trust the people you will be connecting and routing for. This is
a VERY important distinction in the differences between peer-to-peer and
friend to friend.

- Key signing or setting up a PGP web of trust model is in some cases
mandatory.

- Retroshare is difficult to set up for the average user. Every user on
the Retroshare network MUST know how to port forward or the friend
lookup will not function.

- Because it is assumed you already trust the people that you will be
using retroshare to connect to, Retroshare makes no effort to disguise
or hide your IP address from them. In fact, if your IP address changes,
they will get a warning message.

- When operating through the regular Internet, it looks like Retroshare
uses a Distributed Hash Table for IP address lookups and friend finding.
If this is correct this may present a source of metadata leakage. I will
need to look into this some more and find out how it works, because I
don't want to spread F-U-D.

- Retroshare *can be made to* go over I2P, but doing so is very slow and
requires configuration of the I2P Router. You will need to set up your
own tunnels. The documentation for this is a little bit sparse and some
of it is in Spanish. You may need to do a bit of experimentation before
it works. During this time on I2P, friend finding and the DHT can be
turned off, and in this case, Retroshare will function as a true Darknet
which will allow for TLS-secured traffic to be wrapped up within I2P's
native encryption functions. But this is extremely slow and difficult.

- Retroshare is loaded with features and probably hands down has the
most features of any instant messaging bundle. It is VERY good at
distributing large files among friends who trust each other.

- Retroshare's trust model is transitory. Friends-of-friends have a
certain amount of privilege in some areas. For the rest, a lot of it
uses the PGP web of trust.

- The code base has not recently been audited (if ever?). This is the
same situation with I2P, where the weak link might be the client
software and not the protocol.

- If your Retroshare private key is stolen, although technically you
have perfect forward secrecy with TLS, the problem with Retroshare tends
to be that much of the content on the network is distributed among your
friends. It can be difficult to take back down once. So, for instance,
let us say that Alice, Bob, Charlie and Daniel start posting on a
Retroshare messageboard that is private to them. Sometime later, Mallory
steals Alice's plaintext private key. Even if she does not have Alice's
computer, she can still impersonate Alice to Bob, Charlie and Daniel,
and re-synchronize her 'copy' of the messageboard with theirs and see
all of their would-be private communications. If Alice sent movie.mov to
Charlie, and Charlie sent it to Bob, even if Charlie moved movie.mov
out of his share, Mallory can use Alice's private key to impersonate
Alice and re-download movie.mov from Bob instead.

- The more friends you have on your Retroshare network, the more routing
your computer must do and the more bandwidth and processing power the
program will need to function comfortably.

- There is a commandline version of Retroshare that is intended to be
used as a retroshare server. I have never used it, so I cannot comment
on it.

</pre>
</td></tr>

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

<tr>
  <td><a href="https://wire.com">Wire</a></td>
  <td>Android, iOS, MacOS, Windows, Linux, Web</td>
  <td>Text, voice, video</td>
  <td><a href="https://github.com/wireapp">Source code</a></td>
</tr>
<tr><td colspan="4">
<a href="https://crysp.uwaterloo.ca/opinion/wire/">CrySP Wire analysis</a><br>
<pre>
What the server sees and may save:[1]
- Your contact list is saved to the server in plaintext.
- Who you talk to, when, and for how long.
</pre>
</td></tr>

<tr>
  <td><a href="https://www.surespot.me">Surespot</a></td>
  <td>Android, iOS</td>
  <td>Text, voice, images</td>
  <td><a href="https://github.com/surespot">Source code</a></td>
</tr>
  

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
  <td><a href="https://www.wickr.com/personal">Wickr Me</a></td>
  <td><a href="https://me-download.wickr.com/#/version/me">Android, iOS, MacOS, Windows, Ubuntu</a></td>
  <td>Text, video, files</td>
  <td><a href="https://github.com/WickrInc/wickr-crypto-c">Secure Messaging Protocol source</a></td>
</tr>
<tr><td colspan="4">
Partially open source (cypto protocol only)
</td></tr>

<tr>
  <td><a href="https://eleet.im">Eleet</a></td>
  <td><a href="https://eleet.im/download/#tap-mobile">Android, iOS</a>, <a href="https://eleet.im/download/#tab-desktop">MacOS, Windows, Linux</a>, <a href="https://eleet.im/download/#tap-web">Web</a></td>
  <td>Text, group chat, photos, videos, audio files</td>
  <td></td>
</tr>
<tr><td colspan="4">
Eleet is very easy to setup and there is no requirement for an email or phone number.  To add a contact 
you need to acquire their Eleet ID or scan their QR code.  In chats you can see an indicator when someone is typing. 
Encrypted group chats are very easy to create.  Group chats have the option to be anonymous (where 
you will not see anyone's ID only their nickname), and/or temporary where the group chat will be deleted 
from everyone's device at a specified time.<br>
One very nice feature is the ability to create private IDs, which are in addition to your primary ID. 
These private IDs are not linked in any way to your primary one.  Each private ID has a separate list 
of contacts and chats, and they are all accessible without needing to log in and out.
</td></tr>

<tr>
  <td><a href="https://threema.ch">Threema</a></td>
  <td>iOS, Android, Windows Phone, Web</td>
  <td>Text, group chat, voice, files</td>
  <td><a href="https://threema.ch/press-files/cryptography_whitepaper.pdf">Cryptography Whitepaper</a></td>
</tr>
<tr><td colspan="4">
Threema is very easy to setup and use.  Linking to an email or phone number is totally optional. 
To add a contact you need to acquire their Threema ID via a separate channel, search your contacts list for a match 
(hmm, no thanks), or scan their fingerprint QR code in person.  These three methods attach 3 levels of "verification" 
to your contacts:
<ul>
<li>Red- Anonymous (added manually)</li>
<li>Yellow- Matches a contact in your address book</li>
<li>Green- QR code scanned in person</li>
</ul>
This is a nice feature so you can have and easily see different trust levels of your contacts.<br>
It is also very easy to create encrypted group chats with multiple contacts.  All individual and 
group chats will show up in the same list.<br>
Threema is <a href="https://threema.ch/en/faq/source_code">partially open source</a><br>
From the <a href="https://threema.ch/en/faq">FAQ</a>:
<pre>
Which data gets stored at Threema?

Using Threema ought to generate as little data on servers as possible – this is part of the concept.
For that reason, data like e.g. contacts or group chats are stored in a decentralized way on user
devices, instead of on a Threema server. Our servers assume the role of a switch; messages and data
get forwarded, but not permanently stored. Where there is no data, there is nothing to be accessed
or misused. However: without some kind of (temporary) data storage, there cannot be any asynchronous
communication. In the following we will explain what kind of data we store, how we store it and for
how long.

Messages and group chats: As soon as a message has been successfully delivered to the recipient, it
is immediately deleted from the server. All messages and media are transmitted end-to-end encrypted
in Threema. This means: even if someone intercepted your message, it would be completely useless.
Only the intended recipient is able to decrypt and read a message.
No contact lists are stored when synchronizing contacts: The email addresses and phone numbers from
your address book get anonymized (hashed) before they reach the server. Once the comparison is
finished, they are immediately deleted from the server.
Key pairs are generated in a decentralized way on your device. Your private key is never known to
us, and therefore we cannot decrypt any message contents.
Threema doesn't log who is communicating with whom (which Threema IDs are communicating).
</pre>
</td></tr>

<tr>
  <td><a href="https://telegram.org">Telegram</a> (E2EE only in secret chats)</td>
  <td><a href="https://telegram.org/apps">Android, iOS, Windows, MacOS, web</a></td>
  <td>Text, voice, file sharing</td>
  <td><a href="https://telegram.org/faq#q-how-secure-is-telegram">Security</a></td>
</tr>
<tr><td colspan="4">
<pre>
Metadata leakage:[1]
- When you are online or not or whether the application is running or not is
  publicly viewable.
- Who you talk to, when, and the precise time you send a message, and how frequently
  is publicly viewable via commandline tools.
- If an attacker knows your phone number, the attacker will be able to silently log
  your Telegram activity without you knowing about it or being informed they have you
  as a contact.

Stalking via Telegram through the use of Commandline Tools (Flisback, Ola, updated 2015,
  December 16th)
<a href="https://oflisback.github.io/telegram-stalking/">https://oflisback.github.io/telegram-stalking/</a>

Contact Theft through Telegram, Paragraph 9 and 10.
"Operational Telegram"  "The Grugq (assumed name" (Posted November 18th, 2015)
<a href="https://medium.com/@thegrugq/operational-telegram-cbbaadb9013a#.a62knhv8x">https://medium.com/@thegrugq/operational-telegram-cbbaadb9013a#.a62knhv8x</a>

A practical Analysis of the Telegram Messaging Protocol
Jakobsen, Jakob B. (Published September 2015)
<a href="http://cs.au.dk/~jakjak/master-thesis.pdf">http://cs.au.dk/~jakjak/master-thesis.pdf</a>
</pre>
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
  <li>Semaphor- targeted for business, monthly subscription</li>
  <li>Mumble- voice, not text</li>
  <li>Jitsi- video conferencing</li>
</ul>
<br>
<p>To investigate:</p>
<ul>
<li>Facetime, iMessage</li>
<li>Slack</li>
<li>Hoccer https://hoccer.com/de/</li>
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

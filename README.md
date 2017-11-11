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
SMS:
<ul>
<li>Signal<br>
OK let's get this one out of the way first.  If you have a phone, there's almost no way to get away from SMS.  So the best thing you can do is protect your SMS messages at rest with encryption.  Signal also offers excellent end to end encryption between Signal users.  One draw back of Signal is that everyone you connect with will know your phone number.  For people you are comfortable knowing your phone number that is fine, but for those you don't want to give out your number to...<br>
</li>
</ul>
<br>
Messaging apps to use without giving out your phone number:
<ul>
  <li>P2P:</li>
  <ul>
    <li>Ring (eagerly waiting for iOS client)</li>
    <li>Ricochet (desktop only)</li>
    <li>Tox (I had some usability issues and crashing with some clients)</li>
  </ul>
<br>
  <li>Federated or Centralized:</li>
  <ul>
    <li>XMPP with OMEMO</li>
    <li>Keybase.io</li>
    <li>Riot/Matrix (E2EE still in beta)</li>
  </ul>
</ul>
Scoring messaging apps used across multiple platforms:<br>
<table>
<tr>
  <th>Application</th>
  <th width="12%">Additional sharing features- files, photos, etc</th>
  <th width="12%">Group chats</th>
  <th width="12%">Unified UI across platforms</th>
  <th width="12%">Messages sync to all devices</th>
  <th width="12%">Open source</th>
  <th width="12%">Perfect forward secrecy</th>
  <th width="12%">Total score:</th>
</tr>
<tr>
  <td>Riot.im</td>
  <td>0</td><td>1</td><td>1</td><td>1</td><td>1</td><td>?</td><td>4</td>
</tr>
<tr>
  <td>Keybase.io</td>
  <td>0</td><td>1</td><td>1</td><td>1</td><td>1</td><td>?</td><td>4</td>
</tr>
<tr>
  <td>Eleet.im</td>
  <td>1</td><td>1</td><td>1</td><td>1</td><td>0</td><td>?</td><td>4</td>
</tr>
<tr>
  <td>WickrMe</td>
  <td>0</td><td>0</td><td>1</td><td>1</td><td>.5</td><td>1</td><td>3.5</td>
</tr>
<tr>
  <td>XMPP</td>
  <td>.5 (depends on client)</td><td>.5 (depends on client)</td><td>0</td><td>.5 (depends on client)</td><td>1</td><td>?</td><td>2.5</td>
</tr>
<tr>
  <td>Ring.cx</td>
  <td>0</td><td>0</td><td>1</td><td>0</td><td>1</td><td>?</td><td>2</td>
</tr>

</table>

If you're not so strict about being open source try:
<ul>
  <li>Eleet- I am really liking this one</li>
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
  <td><a href="https://ring.cx">Ring</a></td>
  <td><a href="https://ring.cx/en/download">Android, Linux, Mac, Windows (soon iOS)</a></td>
  <td>Text, group chat, voice, video</td>
  <td><a href="https://github.com/savoirfairelinux/">Source Code</a></td>
</tr>
<tr><td colspan="4">
Country of origin: Canada<br>
    Pros:<br>
    On F-Droid<br>
    Multiple platforms<br>
    Not dependent on a phone #<br>
    Cons:<br>
    Android and Mac app still have some usability issues, just out of beta<br>
    <br>
    My verdict: Yes yes yes!<br>
    This is being developed as a side project by Savoir-faire Linux so they know open source!  The clients have a unified experience and are available for most platforms (waiting for iOS).<br>
    This was designed as a P2P app, so messages you send are not synced between your multiple clients.  However messages sent to you do appear on all your clients, making a somewhat confusing stream of conversation when using multiple clients.
</td></tr>

<tr>
  <td><a href="https://ricochet.im">Ricochet</a></td>
  <td><a href="https://ricochet.im/releases/latest/">Windows, Mac, Linux</a></td>
  <td>Text</td>
  <td><a href="https://github.com/ricochet-im/ricochet">Source Code</a></td>
</tr>
<tr><td colspan="4">
    Works over Tor<br>
    Is this still in active development?- <a href="https://github.com/ricochet-im/ricochet/issues/555">Yes</a><br>
    Creates a <a href="https://www.torproject.org/docs/hidden-services.html.en">hidden Tor service</a> to connect P2P.<br>
    <br>
    My verdict: Great option for desktops, mobiles coming soon?<br>
    I love that it is based on Tor hidden services.  I hope that development continues to increase in pace and we see more updates soon.<br>
    Note that this is sill considered an experimental project.
</td></tr>

<tr>
  <td><a href="https://tox.chat">Tox</a></td>
  <td><a href="https://tox.chat/download.html">Windows, Mac, Linux, FreeBSD, iOS, Android</a></td>
  <td>Text, voice, video, screen sharing, file sharing</td>
  <td><a href="https://github.com/TokTok/c-toxcore">toxcore source</a></td>
</tr>
<tr><td colspan="4">
  toxcore was <a href="https://tox.chat/download.html#toktok-c-toxcore">forked</a> to continue development<br>
  Several clients are available and are developed independently of the core.<br>
  <br>
<blockquote>
What is leaked to the world:[1]<br>
- Your IP address and the time you are online is revealed to your contacts. When chatting
  to another contact, you are connecting directly to them.<br>
- Tor activity for contact finding.<br>
- Not sure what else? There may be more. Going to have to read the documentation.
</blockquote>
<br>
My verdict: Try it!<br>
Tox has a lot of promise, the clients need more polishing but they are available for most platforms which will help adoptability.
</td></tr>

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
    Requires physical presence of contacts for initial verification (by design)<br>
    <br>
    My verdict: Good option for specific use case.<br>
    By that I mean it is good if:
    <ul>
      <li>You can meet your contacts in person</li>
      <li>You and your contacts all use Android</li>
      <li>You want the option to be able to communicate outside the standard internet</li>
    </ul>
</td></tr>


<tr><td colspan="4" style="text-align:center"><H2>Federated and Centralized Open Source</H2></td></tr>
  <tr><td><b>Application (notes)</b></td>
  <td><b>Platforms</b></td>
  <td><b>Communication types</b></td>
  <td><b>Websites</b></td></tr>

<tr>
  <td><a href="https://www.signal.org">Signal</a></td>
  <td>Android (<a href="https://signal.org/android/apk/">Direct APK download</a>), iPhone, Desktop</td>
  <td>Text, voice, video, files, images</td>
  <td><a href="https://github.com/WhisperSystems">Source Code</a>, <a href="https://www.signal.org/docs/">Technical docs</a></td>
</tr>
<tr><td colspan="4">
Requires a phone number to register
<blockquote>
What the server sees:[1]<br>
- The phone number used for your registration.<br>
- SHA-2 Hashes of your contacts' telephone numbers to check for a match. OWS claims
  to delete this as soon as it is no longer needed.<br>
<br>
What Signal claims to keep:<br>
- The day you first joined the service<br>
- The last day you used it.<br>
<br>
Disadvantages:<br>
- People must know your phone number. It is possible to register a burner number or
  a VOIP number, but this is an advanced-use case.
</blockquote>
<br>
My verdict: Best SMS replacement app<br>
This app may be the easiest to convince other people to use. However it requires the use of your phone number as an identifier, so if you are not comfortable giving some people your phone number there are better options to communicate with them.
</td></tr>

<tr>
  <td><a href="https://xmpp.org">XMPP</a> (with <a href="https://wiki.xmpp.org/web/OTR">OTR</a> or OMEMO)</td>
  <td>Linux, Windows, MacOS, Android, iOS</td>
  <td>Text, group chat</td>
  <td><a href="https://xmpp.org/getting-started/">Getting Started</a></td>
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
<blockquote>
What the server sees:[1]<br>
- Your plaintext chats unless you use encryption such as OTR, PGP, or OMEMO.<br>
- Your contact list is saved to the server in plaintext<br>
- Precise time you logged in or out<br>
- Precise time you sent any messages to a contact and what messages they send you.<br>
- Whether you are online or not, and your status.<br>
- Who you contacted, when, and how frequently.<br>
- SHA-1 hash of your password. Improperly configured servers may store passwords in plaintext.
</blockquote>
<br>
My verdict: The best option for a wide base of users.<br>
XMPP is a protocol, and clients are built on top of that so there are many options across all platforms which will help adoptability.<br>
One drawback is the clients are all different so there is a lack of consistency in experience and features across platforms.
</td></tr>

<tr>
  <td><a href="https://www.keybase.io">Keybase.io</a></td>
  <td><a href="https://keybase.io/download">Android, iOS, MacOS, Windows, Linux</a></td>
  <td>Text, group chat, file sharing</td>
  <td><a href="https://github.com/keybase">Source code</a></td>
</tr>
<tr><td colspan="4">
  You can also verify other website identities, GPG keys, domains, etc that you own.<br>
  <br>
  My verdict: Great for chat and other uses<br>
  Keybase has several unique features, which now also includes secured personal and group file storage and sharing and encrypted git.  It is also very easy for someone new to PGP to create a new key for themselves.
</td></tr>

<tr>
  <td><a href="https://about.riot.im">Riot/Matrix</a></td>
  <td><a href="https://about.riot.im/downloads/">Android, iOS, Linux, Mac, Windows, Web</a></td>
  <td>Text, voice, video, file sharing</td>
  <td><a href="https://github.com/vector-im">Source code</a></td>
</tr>
<tr><td colspan="4">
Riot <a href="https://about.riot.im/security/">Security</a> (E2EE still in beta)<br>
  The web app can be used over Tor (thanks lwinch2006)<br>
  <br>
  My verdict: Great social platform<br>
  Riot/Matrix is a great way to meet new people, and with E2EE (in beta) for individual and group chats it offers a way to go dark for private conversations.<br>
  E2EE is still in the works and takes a bit of manual effort to get setup in chats, but that should be improving with time.
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
  <td><a href="http://retroshare.net">RetroShare</a></td>
  <td><a href="http://retroshare.net/downloads.html">Windows, Mac, Linux</a></td>
  <td>Text, voice, video, email, file sharing</td>
  <td><a href="https://github.com/RetroShare/RetroShare">Source code</a></td>
</tr>
<tr><td colspan="4">
<blockquote>
What is leaked to the world when using the DHT.[1]<br>
- Your IP address.<br>
- The IP addresses that you are connecting to.<br>
Optionally, Retroshare may be configured to tunnel through I2P or Tor
with friend finding turned off to function as a true darknet. This
however, is slow, unreliable, high-latency, and very difficult to set up.<br>
<br>
- Retroshare may appear to use PGP, but what actually seems to be
happening under the hood is that it's using the RSA keys to sign
ephemeral keys which are then used to establish connections to your
friends via perfect forward secrecy. The PGP parts of it look like they
are used only for certifying and authentication, and are not used to
encrypt the data.<br>
<br>
- Certificate authorities are not used, the networks are fully
friend-to-friend. This is markedly different from peer-to-peer because
it is expected in a friend-to-friend network, you already know, and
already trust the people you will be connecting and routing for. This is
a VERY important distinction in the differences between peer-to-peer and
friend to friend.<br>
<br>
- Key signing or setting up a PGP web of trust model is in some cases
mandatory.<br>
<br>
- Retroshare is difficult to set up for the average user. Every user on
the Retroshare network MUST know how to port forward or the friend
lookup will not function.<br>
<br>
- Because it is assumed you already trust the people that you will be
using retroshare to connect to, Retroshare makes no effort to disguise
or hide your IP address from them. In fact, if your IP address changes,
they will get a warning message.<br>

- When operating through the regular Internet, it looks like Retroshare
uses a Distributed Hash Table for IP address lookups and friend finding.
If this is correct this may present a source of metadata leakage. I will
need to look into this some more and find out how it works, because I
don't want to spread F-U-D.<br>
<br>
- Retroshare *can be made to* go over I2P, but doing so is very slow and
requires configuration of the I2P Router. You will need to set up your
own tunnels. The documentation for this is a little bit sparse and some
of it is in Spanish. You may need to do a bit of experimentation before
it works. During this time on I2P, friend finding and the DHT can be
turned off, and in this case, Retroshare will function as a true Darknet
which will allow for TLS-secured traffic to be wrapped up within I2P's
native encryption functions. But this is extremely slow and difficult.<br>
<br>
- Retroshare is loaded with features and probably hands down has the
most features of any instant messaging bundle. It is VERY good at
distributing large files among friends who trust each other.<br>
<br>
- Retroshare's trust model is transitory. Friends-of-friends have a
certain amount of privilege in some areas. For the rest, a lot of it
uses the PGP web of trust.<br>
<br>
- The code base has not recently been audited (if ever?). This is the
same situation with I2P, where the weak link might be the client
software and not the protocol.<br>
<br>
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
Alice and re-download movie.mov from Bob instead.<br>
<br>
- The more friends you have on your Retroshare network, the more routing
your computer must do and the more bandwidth and processing power the
program will need to function comfortably.<br>
<br>
- There is a commandline version of Retroshare that is intended to be
used as a retroshare server. I have never used it, so I cannot comment
on it.
</blockquote>
</td></tr>

<tr>
  <td><a href="https://wire.com">Wire</a></td>
  <td>Android, iOS, MacOS, Windows, Linux, Web</td>
  <td>Text, voice, video</td>
  <td><a href="https://github.com/wireapp">Source code</a></td>
</tr>
<tr><td colspan="4">
<a href="https://medium.com/@wireapp/open-sourcing-wire-server-code-ef7866a731d5">Server code open sourced</a><br>
<a href="https://crysp.uwaterloo.ca/opinion/wire/">CrySP Wire analysis</a>:
<ul>
  <li>Wire client sends the unencrypted, unhashed password to the central server over TLS, the server hashes the plaintext password with scrypt, and the hash is compared to the hash stored by the server.		This process leaks the user's password to the central server; the server operators (or anyone who compromises the server) could log all of the plaintext passwords as users authenticate.</li>
  <li>The desktop application is implemented as a packaged web application</li>
</ul>
<blockquote>
What the server sees and may save:[1]<br>
- Your contact list is saved to the server in plaintext.<br>
- Who you talk to, when, and for how long.
</blockquote>
</td></tr>

<tr>
  <td><a href="https://www.surespot.me">Surespot</a></td>
  <td>Android, iOS</td>
  <td>Text, voice, images</td>
  <td><a href="https://github.com/surespot">Source code</a></td>
</tr>
<tr><td colspan="4">
Development seems to have ceased in May 2017.<br>
<a href="https://www.surespot.me/documents/threat.html">Data and threat analysis</a>
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
<tr><td colspan="4">
Country of origin: France?<br>
TwinMe is easy to setup and to connect with another TwinMe user you can either scan their QR code in person or send them an invite link.<br>
The interface is professional looking, though the iOS version seems more consistant with the host OS than the Android version.  For example 
the Android client does not have autocorrect so typing behaves differently than if you are used to autocorrect.<br>
One cool feature is the ability to stream music from your device to your contact's device.<br>
On Android Google Play Services are not required.  The Android version I first tried from the Amazon app store would not launch at all. 
The version from the Google Play Store (downloaded via Yalp) did run.
</td></tr>

<tr>
  <td><a href="http://stealthchat.com">StealthChat</a></td>
  <td>Android, iOS</td>
  <td>Text, voice, pictures</td>
  <td></td>
</tr>
<tr><td colspan="4">
Country of origin: USA<br>
Self destruct messages<br>
Requires a phone number to register, uses the phone numbers in your contacts list.
</td></tr>

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
Country of origin: USA<br>
Partially open source (cypto protocol only)<br>
WickrMe synchronizes your chats across all your devices.<br>
There are no group chats and not many unique features, but as a basic chat client it works very well.<br>
Conversations expire after a set time or can be set to erase once read.
</td></tr>

<tr>
  <td><a href="https://eleet.im">Eleet</a></td>
  <td><a href="https://eleet.im/download/#tap-mobile">Android, iOS</a>, <a href="https://eleet.im/download/#tab-desktop">MacOS, Windows, Linux</a>, <a href="https://eleet.im/download/#tap-web">Web</a></td>
  <td>Text, group chat, photos, videos, audio files</td>
  <td></td>
</tr>
<tr><td colspan="4">
Country of origin: Scotland, UK<br>
Eleet is very easy to setup and there is no requirement for an email or phone number.  To add a contact 
you need to acquire their Eleet ID or scan their QR code.  In chats you can see an indicator when someone is typing. 
Encrypted group chats are very easy to create.  Group chats have the option to be anonymous (where 
you will not see anyone's ID only their nickname), and/or temporary where the group chat will be deleted 
from everyone's device at a specified time.<br>
One very nice feature is the ability to create private IDs, which are in addition to your primary ID. 
These private IDs are not linked in any way to your primary one.  Each private ID has a separate list 
of contacts and chats, and they are all accessible without needing to log in and out.<br>
The desktop clients will sync up all messages so you can transition between devices and see all messages.
</td></tr>

<tr>
  <td><a href="https://threema.ch">Threema</a></td>
  <td>iOS, Android, Windows Phone, Web</td>
  <td>Text, group chat, voice, files</td>
  <td><a href="https://threema.ch/press-files/cryptography_whitepaper.pdf">Cryptography Whitepaper</a></td>
</tr>
<tr><td colspan="4">
Country of origin: Switzerland<br>
Threema is very easy to setup and use.  Linking to an email or phone number is totally optional. 
To add a contact you need to acquire their Threema ID via a separate channel, search your contacts list for a match,
 or scan their fingerprint QR code in person.  These three methods attach 3 levels of "verification" 
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
<blockquote cite="https://threema.ch/en/faq">
Which data gets stored at Threema?<br>
<br>
Using Threema ought to generate as little data on servers as possible – this is part of the concept.
For that reason, data like e.g. contacts or group chats are stored in a decentralized way on user
devices, instead of on a Threema server. Our servers assume the role of a switch; messages and data
get forwarded, but not permanently stored. Where there is no data, there is nothing to be accessed
or misused. However: without some kind of (temporary) data storage, there cannot be any asynchronous
communication. In the following we will explain what kind of data we store, how we store it and for
how long.<br>
<br>
Messages and group chats: As soon as a message has been successfully delivered to the recipient, it
is immediately deleted from the server. All messages and media are transmitted end-to-end encrypted
in Threema. This means: even if someone intercepted your message, it would be completely useless.
Only the intended recipient is able to decrypt and read a message.<br>
No contact lists are stored when synchronizing contacts: The email addresses and phone numbers from
your address book get anonymized (hashed) before they reach the server. Once the comparison is
finished, they are immediately deleted from the server.<br>
Key pairs are generated in a decentralized way on your device. Your private key is never known to
us, and therefore we cannot decrypt any message contents.<br>
Threema doesn't log who is communicating with whom (which Threema IDs are communicating).
</blockquote>
</td></tr>

<tr>
  <td><a href="https://hoccer.com">Hoccer</a></td>
  <td><a href="https://hoccer.com/#section-download">Android, iOS</a></td>
  <td>Text, file sharing</td>
  <td><a href="https://hoccer.com/faq/">FAQ</a></td>
</tr>
<tr><td colspan="4">
Country of origin: Germany<br>
Only works on a single device
</td></tr>

<tr>
  <td><a href="https://www.sims.me">SIMSme</a></td>
  <td><a href="https://www.sims.me/en#Download">Android, iOS</a></td>
  <td>Text, group chat, images, videos, location, contacts</td>
  <td><a href="https://www.sims.me/data-protection">Data Protection</a></td>
</tr>
<tr><td colspan="4">
Country of origin: Germany<br>
Developed by the Deutsche Post, servers are located in Germany<br>
The SIMSme encryption key is tied to the phone and cannot be transfered to another.  Requires a phone number to register.<br>
Invite contacts based on their phone number.  SIMSme checks your address book for existing registered users.<br>
Three levels of contact trust- High, Medium and Low.<br>
Self destructing messages.<br>
It gives an error on Android without Google Play Services that it won't run, but it seems to work.
</td></tr>

<tr>
  <td><a href="https://telegram.org">Telegram</a> (E2EE only in secret chats)</td>
  <td><a href="https://telegram.org/apps">Android, iOS, Windows, MacOS, web</a></td>
  <td>Text, voice, file sharing</td>
  <td><a href="https://telegram.org/faq#q-how-secure-is-telegram">Security</a></td>
</tr>
<tr><td colspan="4">
Country of origin: Russia, now Dubai<br>
<blockquote>
Metadata leakage:[1]<br>
- When you are online or not or whether the application is running or not is
  publicly viewable.<br>
- Who you talk to, when, and the precise time you send a message, and how frequently
  is publicly viewable via commandline tools.<br>
- If an attacker knows your phone number, the attacker will be able to silently log
  your Telegram activity without you knowing about it or being informed they have you
  as a contact.<br>
<br>
Stalking via Telegram through the use of Commandline Tools (Flisback, Ola, updated 2015,
  December 16th)<br>
<a href="https://oflisback.github.io/telegram-stalking/">https://oflisback.github.io/telegram-stalking/</a><br>
<br>
Contact Theft through Telegram, Paragraph 9 and 10.<br>
"Operational Telegram"  "The Grugq (assumed name" (Posted November 18th, 2015)<br>
<a href="https://medium.com/@thegrugq/operational-telegram-cbbaadb9013a#.a62knhv8x">https://medium.com/@thegrugq/operational-telegram-cbbaadb9013a#.a62knhv8x</a><br>
<br>
A practical Analysis of the Telegram Messaging Protocol<br>
Jakobsen, Jakob B. (Published September 2015)<br>
<a href="http://cs.au.dk/~jakjak/master-thesis.pdf">http://cs.au.dk/~jakjak/master-thesis.pdf</a>
</blockquote>
</td></tr>

<tr>
  <td><a href="https://www.viber.com">Viber</a></td>
  <td>Android, iOS, Mac, Windows, Linux</td>
  <td>Text, group messaging, voice and video calls, photos</td>
  <td><a href="https://support.viber.com">Support</a>,<br>
  <a href="https://www.viber.com/security-overview">Security Overview</a></td>
</tr>
<tr><td colspan="4">
Thanks to "C" for pointing out Viber really is E2EE.  They don't mention that specifically on their main page, you have to go to their support site to read about it.<br>
Requires a phone number to register, add contacts using their phone number.<br>
Custom protocol- from the security overview:
<blockquote>
Viber’s protocol uses the same concepts of the “double ratchet” protocol used in
Open Whisper Systems Signal application, however, Viber’s implementation was
developed from scratch and does not share Signal’s source code.
</blockquote>
</td></tr>

<tr>
  <td><a href="https://getconfide.com">Confide</a></td>
  <td><a href="https://getconfide.com/download">Android, iOS, Mac, Windows</a></td>
  <td>Text, group messaging, voice and video messages, file sharing</td>
  <td><a href="https://getconfide.com/faq">FAQ</a>,<br>
  <a href="https://static.getconfide.com/audits/Confide-PT_A4.ENG.0001.02.pdf">Security Audit</a></td>
</tr>
<tr><td colspan="4">
Messages are destroyed after they are read
<blockquote>
Information provided by "C":<br>
<a href="https://www.wired.com/2017/03/confide-security-holes/">That Encrypted Chat App the White House Liked? Full of Holes</a><br>
Which links to: <a href="https://blog.quarkslab.com/make-confide-great-again-no-we-cannot.html">Make Confide great again? No, we cannot</a>
</blockquote>
<br>
My verdict: Stay Away!<br>
It is very concerning that such lax security practices (weak password rules, no message authentication or integrity validation) were allowed to be a part of the design in the first place.<br>
Also the desktop clients are written in JavaScript which is easily modified to bypass security checks.<br>
Did they fix these issues?  Maybe but without open code to inspect we cannot know.  
</td></tr>

</table>

<p>Apps that are not E2EE:</p>
<ul>
  <li>Facebook Messenger</li>
  <li>Google Hangouts, Allo, Duo</li>
  <li>Yahoo Messenger, AIM, ICQ</li>
  <li>Skype</li>
  <li>Trello</li>
</ul>
<br>
<p>Apps not recommended for other reasons:</p>
<ul>
  <li>Facetime, iMessage- iOS only, closed source, data saved on Apple servers</li>
  <li>WhatsApp- <a href="https://www.eff.org/deeplinks/2016/10/where-whatsapp-went-wrong-effs-four-biggest-security-concerns">EFF's concerns</a>:<br>
    -Unencrypted backups at rest<br>
    -Data sharing with Facebook
  </li>
  <li>Semaphor- targeted for business, monthly subscription</li>
  <li>Mumble- Voice chat for gaming. You can send text and links but that is not its primary intent.</li>
  <li>Jitsi- video conferencing</li>
  <li>Bubcon- <a href="https://bubcon.com/datenschutz-app/?lang=en">Phone# required, collects your contacts info</a><br>
   -Android only (Oct 2017), single device only<br>
   -Messages stored decrypted at rest
  </li>
  <li>Line (https://line.me) No information about security on website, does not seem to be a focus at all although there are articles online claiming they are E2EE.</li>
  <li>WeChat (http://www.wechat.com) No information about security on website, requires a phone number to register.</li>
</ul>
<br>
<p>To investigate:</p>
<ul>
<li>https://bitchat.im- Windows and Ubuntu</li>
<li>https://www.chatgrape.com/open-source - All platforms except Linux, monthly subscription</li>
<li>Slack</li>
<li>Disa- http://disa.im/index.html</li>
<li>FireChat https://www.opengarden.com/firechat.html</li>
<li>OnionShare</li>
<li>Chiffry- https://www.chiffry.de</li>
<li>GDATA Secure Chat- https://www.gdata.de/mobile</li>
<li>Brabbler- https://www.brabbler.ag/index-de.html</li>
<li>Kullo- https://www.kullo.net/de/#start</li>

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

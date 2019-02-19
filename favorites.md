---
layout: single
title: My list of favorite secure messaging apps
---
<h2>My current top picks:</h2><br>
Criteria:
<ul>
  <li>This list is focused on instant messaging and chatting as the primary usage of the app</li>
  <li>Clients on multiple platforms preferred</li>
  <li>Does not expose your phone number or email address to other users</li>
  <li>Does not leak data (pictures or other data saved unencrypted in browseable folders)</li>
  <li>Has ephemeral messages (encryption keys destroyed after a set time)</li>
  <li>Has contact verification</li>
  <li>Testing done on both Android and iOS when possible.  See my <a href="/about.html#testsetup">testing setup</a></li>
</ul>
SMS Apps:
<ul>
  <li>{% include generate_app_link.html app_name="signal" %}<br>
    OK let's get this one out of the way first.  If you have a phone, there's almost no way to get away from SMS.  So the best thing you can do is protect your SMS messages at rest with encryption.  Signal also offers excellent end to end encryption between Signal users.  One draw back of Signal is that everyone you connect with will know your phone number, but for people you are comfortable knowing your phone number that is fine.<br>
  </li>
  <li>Runner up: {% include generate_app_link.html app_name="silence" %}<br>
    If you don't want to use Signal as a messaging app then I recommend getting Silence just for SMS messages.  It will locally encrypt the SMS database on your phone.  You can also send encrypted SMS messages to other Silence users.  Since Silence only uses SMS it is not dependent on any servers like Signal is.
  </li>
</ul>
<br>
Messaging apps listed here do not expose your phone number or email address.  Notes within [brackets] are potential negative attributes:
<ul>
  <li>Top Tier Recommendations:</li>
  <ul>
    <li>{% include generate_app_link.html app_name="wire" %}- [Beware of possible high battery usage on older Android versions or Android forks without Play Services]</li>
    <li>{% include generate_app_link.html app_name="wickrme" %}- All messages expire [Based in USA]</li>
    <li>{% include generate_app_link.html app_name="safeswiss" %}- P2P, based in Switzerland</li>
  </ul>
  <li>Second Tier (misses some criteria):</li>
  <ul>
    <li>{% include generate_app_link.html app_name="threema" %}- Based in Switzerland [No PFS or ephemeral messages]</li>
    <li>{% include generate_app_link.html app_name="twinme" %}- P2P, based in Germany [No ephemeral messages or contact verification]</li>
  </ul>

  <li>Third Tier (keep an eye on these):</li>
  <ul>
    <li>{% include generate_app_link.html app_name="briar" %}- P2P, can use Tor [Android only, text only, no ephemeral messages]</li>
    <li>{% include generate_app_link.html app_name="keybase" %}- [Based in USA, only &quot;exploding&quot; messages are PFS, no contact verification]</li>
    <li>{% include generate_app_link.html app_name="tungsten" %}- New app still in beta but this shows lots of promise.  Uses the TOR network for anonymous profiles, synchronizes across multiple devices, multiple personas, based in Germany. [No ephemeral messages or contact verification]</li>
    <li>{% include generate_app_link.html app_name="babelnet" %}- Very nice syncing between multiple devices, based outside of the 14 eyes [User interface needs clarified wording, trouble connecting with LineageOS]</li>
    <li>{% include generate_app_link.html app_name="conversations" %} or {% include generate_app_link.html app_name="pixart" %}- Based in Germany [Android Only, no ephemeral messages]</li>
  </ul>
  <li id="caution">Use with caution:<br>
  <ul>
     <li>{% include generate_app_link.html app_name="eleet" %}- [Based in the UK, no contact verification]</li>
    <li>{% include generate_app_link.html app_name="riot" %}- [E2EE still in beta, Based in the UK, no ephemeral messages]</li>
  </ul>
  December 2018: Recently there have been some troubling laws passed and articles written in the UK and Australia (part of the <a href="https://www.privacytools.io/#ukusa">5 eyes countries</a>) that may cause issues with trust in applications developed in those countries.  Both countries now seem to be pushing for backdoor access for government surveillance to be built into secure messaging applications.  Not only will this weaken or break End to End security, but apps that are not open source from those countries may no longer be trusted and may be used for a mass surveillance program.  Here are some recent articles.<br>
  <a href="https://www.lawfareblog.com/principles-more-informed-exceptional-access-debate">Principles for a More Informed Exceptional Access Debate</a><br>
  <blockquote>
  In a world of encrypted services, a potential solution could be to go back a few decades. It’s relatively easy for a <u>service provider to silently add a law enforcement participant to a group chat or call</u>. The service provider usually controls the identity system and so really decides who’s who and which devices are involved - they’re usually involved in introducing the parties to a chat or call. You end up with everything still being end-to-end encrypted, but there’s an extra ‘end’ on this particular communication. This sort of solution seems to be no more intrusive than the virtual crocodile clips that our democratically elected representatives and judiciary authorise today in traditional voice intercept solutions and certainly doesn’t give any government power they shouldn’t have.<br>
<br>
We’re not talking about weakening encryption or defeating the end-to-end nature of the service. In a solution like this, we’re normally talking about <u>suppressing a notification on a target’s device</u>, and only on the device of the target and possibly those they communicate with. That’s a very different proposition to discuss and you don’t even have to touch the encryption.<br>
&nbsp;&nbsp;-Ian Levy is the technical director of the National Cyber Security Centre, a part of GCHQ.<br>
&nbsp;&nbsp;-Crispin Robinson is the technical director for cryptanalysis at GCHQ.
</blockquote>
<br>
  <a href="https://arstechnica.com/tech-policy/2018/12/australia-passes-new-law-to-thwart-strong-encryption/">Australia passes new law to thwart strong encryption</a><br>
  <blockquote>
  The new law, which has been pushed for since at least 2017, requires that companies provide a way to get at encrypted communications and data via a warrant process. It also imposes fines of up to A$10 million for companies that do not comply and A$50,000 for individuals who do not comply. In short, the law thwarts (or at least tries to thwart) strong encryption.<br>
<br>
  Companies who receive one of these warrants have the option of either complying with the government or waiting for a court order. However, by default, the orders are secret, so companies would not be able to tell the public that they had received one.
  </blockquote>
  </li>
</ul>
<br>
<br>
<h2>How about some rankings?</h2><br>
The following scoring table includes messaging apps that can be used across multiple platforms that synchronize conversations to all devices:<br>
<table>
  <tr>
    <th>Application</th>
    <th width="8%">Additional sharing features- files, photos, etc</th>
    <th width="8%">Group chats</th>
    <th width="8%">Unified UI across platforms</th>
    <th width="8%">Messages sync to all devices</th>
    <th width="8%">Open source</th>
    <th width="8%">Perfect forward secrecy</th>
    <th width="8%">Ephemeral Messages</th>
    <th width="8%">Contact Verification</th>
    <th width="8%">Based outside the <a href="https://www.privacytools.io/#ukusa">5 eyes</a>: +.5<br>
      Based outside the 14 eyes: +.5</th>
    <th width="8%">Total score:</th>
  </tr>
  <tr>
    <td>{% include generate_app_link.html app_name="wire" %}</td>
    <td>1</td><td>1</td><td>1</td><td>1</td><td>1</td><td>1</td><td>1</td><td>1</td><td>1 (Switzerland)</td><td>9</td>
  </tr>
  <tr>
    <td>{% include generate_app_link.html app_name="babelnet" %}</td>
    <td>1</td><td>1</td><td>1</td><td>1</td><td>0</td><td>1</td><td>1</td><td>1</td><td>1 (Czech Republic)</td><td>8</td>
  </tr>
  <tr>
    <td>{% include generate_app_link.html app_name="wickrme" %}</td>
    <td>1</td><td>1</td><td>1</td><td>1</td><td>.5</td><td>1</td><td>1</td><td>1</td><td>0 (USA)</td><td>7.5</td>
  </tr>
  <tr style='background: pink'>
    <td>{% include generate_app_link.html app_name="riot" %} (<a href="#caution">Use with Caution</a>)</td>
    <td>1</td><td>1</td><td>1</td><td>1</td><td>1</td><td>1</td><td>0</td><td>1</td><td>0 (UK)</td><td>7</td>
  </tr>
  <tr>
    <td>{% include generate_app_link.html app_name="keybase" %}</td>
    <td>1</td><td>1</td><td>1</td><td>1</td><td>1</td><td>.5 (exploding messages)</td><td>1</td><td>0</td><td>0 (USA)</td><td>6.5</td>
  </tr>
  <tr style='background: pink'>
    <td>{% include generate_app_link.html app_name="eleet" %} (<a href="#caution">Use with Caution</a>)</td>
    <td>1</td><td>1</td><td>1</td><td>1</td><td>0</td><td>1</td><td>1</td><td>0</td><td>0 (UK)</td><td>6</td>
  </tr>
  <tr>
    <td>{% include generate_app_link.html app_name="tungsten" %}</td>
    <td>1</td><td>1</td><td>1</td><td>1</td><td>0</td><td>1</td><td>0</td><td>0</td><td>.5 (Germany)</td><td>5.5</td>
  </tr>

</table>

The following scoring table includes messaging apps used on a single device:<br>
<table>
  <tr>
    <th>Application</th>
    <th width="8%">Additional sharing features- files, photos, etc</th>
    <th width="8%">Group chats</th>
    <th width="8%">Open source</th>
    <th width="8%">Perfect forward secrecy</th>
    <th width="8%">Ephemeral Messages</th>
    <th width="8%">Contact Verification</th>
    <th width="8%">Clients on multiple platforms</th>
    <th width="8%">Based outside the <a href="https://www.privacytools.io/#ukusa">5 eyes</a>: +.5<br>
      Based outside the 14 eyes: +.5</th>
    <th width="8%">Total score:</th>
  </tr>
  <tr>
    <td>{% include generate_app_link.html app_name="wire" %}</td>
    <td>1</td><td>1</td><td>1</td><td>1</td><td>1</td><td>1</td><td>1</td><td>1 (Switzerland)</td><td>8</td>
  </tr>
  <tr>
    <td>{% include generate_app_link.html app_name="babelnet" %}</td>
    <td>1</td><td>1</td><td>0</td><td>1</td><td>1</td><td>1</td><td>1</td><td>1 (Czech Republic)</td><td>7</td>
  </tr>
  <tr>
    <td>{% include generate_app_link.html app_name="safeswiss" %}</td>
    <td>1</td><td>1</td><td>0</td><td>1</td><td>1</td><td>1</td><td>1</td><td>1 (Switzerland)</td><td>7</td>
  </tr>
  <tr>
    <td>{% include generate_app_link.html app_name="wickrme" %}</td>
    <td>1</td><td>1</td><td>.5</td><td>1</td><td>1</td><td>1</td><td>1</td><td>0 (USA)</td><td>6.5</td>
  </tr>
  <tr>
    <td>{% include generate_app_link.html app_name="threema" %}</td>
    <td>1</td><td>1</td><td>.5</td><td>.5 (only on the network layer)</td><td>0</td><td>1</td><td>1</td><td>1 (Switzerland)</td><td>6</td>
  </tr>
  <tr style='background: pink'>
    <td>{% include generate_app_link.html app_name="riot" %} (<a href="#caution">Use with Caution</a>)</td>
    <td>1</td><td>1</td><td>1</td><td>1</td><td>0</td><td>1</td><td>1</td><td>0 (UK)</td><td>6</td>
  </tr>
  <tr>
    <td>{% include generate_app_link.html app_name="keybase" %}</td>
    <td>1</td><td>1</td><td>1</td><td>.5 (exploding messages)</td><td>1</td><td>0</td><td>1</td><td>0 (USA)</td><td>5.5</td>
  </tr>
  <tr>
    <td>{% include generate_app_link.html app_name="briar" %}</td>
    <td>0</td><td>1</td><td>1</td><td>1</td><td>0</td><td>1</td><td>0</td><td>1</td><td>5</td>
  </tr>
  <tr style='background: pink'>
    <td>{% include generate_app_link.html app_name="eleet" %} (<a href="#caution">Use with Caution</a>)</td>
    <td>1</td><td>1</td><td>0</td><td>1</td><td>1</td><td>0</td><td>1</td><td>0 (UK)</td><td>5</td>
  </tr>
  <tr>
    <td>{% include generate_app_link.html app_name="conversations" %}</td>
    <td>1</td><td>1</td><td>1</td><td>.5 (OMEMO only)</td><td>0</td><td>1</td><td>0</td><td>.5 (Germany)</td><td>5</td>
  </tr>
  <tr>
    <td>{% include generate_app_link.html app_name="twinme" %}</td>
    <td>1</td><td>1</td><td>0</td><td>1</td><td>0</td><td>0</td><td>1</td><td>.5 (Germany)</td><td>4.5</td>
  </tr>
  <tr>
    <td>{% include generate_app_link.html app_name="tungsten" %}</td>
    <td>1</td><td>1</td><td>0</td><td>1</td><td>0</td><td>0</td><td>1</td><td>.5 (Germany)</td><td>4.5</td>
  </tr>

</table>

---
layout: single
title: My list of favorite secure messaging apps
---
<h2>My current top picks:</h2><br>
Here is a list of the criteria I use to pick the best options. Each app may not have all of these characteristics, but the more that the app has of these in the list the better it will score. Testing is done on both Android and iOS when possible.  See my <a href="/about.html#testsetup">testing setup</a>.
<ul>
  <li>This list is focused on instant messaging and chatting as the primary usage of the app</li>
  <li>Apps without trackers given preference</li>
  <li>Clients on multiple platforms preferred</li>
  <li>Does not expose personal information (for example phone number or email) to other users</li>
  <li>Does not leak data (pictures or other data saved unencrypted in browseable folders)</li>
  <li>Has ephemeral messages (encryption keys destroyed after a set time)</li>
  <li>Has contact verification through key fingerprint or other method</li>
</ul>

<h3>Scoring system:</h3>
Beside each application you will see 4 numbers in colored boxes.  The meaning of these numbers follows:<br>

<span class="w3-tag w3-xlarge w3-round-large w3-red ">1</span>
 This is the lowest score, which means the application does not provide any protection in this category.
<br>
<span class="w3-tag w3-xlarge w3-round-large w3-orange ">2</span>
 This score means the application provides some protection in this category.
<br>
<span class="w3-tag w3-xlarge w3-round-large w3-yellow ">3</span>
 This score means the application provides protection for many items in this category.
<br>
<span class="w3-tag w3-xlarge w3-round-large w3-green ">4</span>
 This score means the application provides complete or almost complete protection in this category.
<br>
<br>
The 4 categories used are:
<ul>
<li>Privacy of your messages: This means that the contents of your encrypted message are safe from being decrypted by anyone who does not have the decryption key, and they are protected from future brute force decryption.</li>
<li>Privacy of your identity: Information which may reveal your true identity is not exposed by using the application.</li>
<li>Integrity of the system: The infrastructure that the application runs on is trustworthy and messages can be verified to be unaltered.</li>
<li>Resistance to disruption: It would be difficult for any one agent to disable the messaging system, for example by targeting the system's servers.</li>
</ul>

<h3>Country of Jurisdiction:</h3>
Another aspect of each messenger to consider is the legal jurisdiction each app is subject to.  This is usually determined by the incorporated status and country of the organization that controls the servers and codebase for the messaging system.  Physical server location is not always a factor, for example a server located anywhere in the world is still considered under the jurisdiction of the country where the controlling organization is incorporated.<br />
There are various international intelligence sharing agreements, the most well known being the so called &quot;5 eyes&quot;, &quot;9 eyes&quot; and &quot;14 eyes&quot; countries.  If your data is protected well enough (encryption) and you are able to remain anonymous online then the country of jurisdiction may not be the primary deciding factor for everyday citizens.  But if you require extra security the jurisdiction may be more important.  You can read more about the &quot;eyes&quot; at <a href="https://restoreprivacy.com/5-eyes-9-eyes-14-eyes/">https://restoreprivacy.com/5-eyes-9-eyes-14-eyes/</a>.

<div class="w3-row">
	<h2><strong>Level 1: Beginner</strong></h2>
	<p>Welcome to your new journey into privacy.  Everyone should install Signal as the first step towards a more private lifestyle.</p>
</div>
<div class="w3-row-padding">
  {% include favorites_card.html app_name="signal" %}
</div>

<br>
<div class="w3-row">
  <h2><strong>Level 2: More anonymous, but centralized</strong></h2>
</div>
<div class="w3-row-padding">
  {% include favorites_card.html app_name="threema" %}
  {% include favorites_card.html app_name="bbme" %}
</div>

<br>
<div class="w3-row">
	<h2><strong>Level 3: Peer to Peer or Decentralized</strong></h2>
</div>
<div class="w3-row-padding">
  {% include favorites_card.html app_name="twinme" %}
  {% include favorites_card.html app_name="conversations" %}
</div>

<br>
<div class="w3-row">
	<h2><strong>Level 4: Alternative Networks</strong></h2>
</div>
<div class="w3-row-padding">
  {% include favorites_card.html app_name="briar" %}
  {% include favorites_card.html app_name="onionshare" %}
</div>

<br>
<div class="w3-row">
	<h2><strong>Level 5: Experimental (know what you're doing)</strong></h2>
</div>
<div class="w3-row-padding">
  {% include favorites_card.html app_name="session" %}
  {% include favorites_card.html app_name="cabal" %}
</div>


<p>
<h2>Details on scores for each app:</h2>
<table class="w3-table-all w3-small w3-centered">
<tr>
<th>App</th>
<th colspan="6" class="w3-grey">Privacy of Messages</th>
<th colspan="4">Privacy of Identity</th>
<th colspan="5" class="w3-grey">Integrity of the System</th>
<th colspan="5">Resistance to Disruption</th>
</tr>
<tr>
 <th width="10%" class="w3-right-align"></th>
 <th width="4%">
 <span class="w3-tooltip">
		<span class="w3-round">EM</span>
		<span style="position:absolute;left:-40px;bottom:36px" class="w3-text w3-tag w3-round w3-large">Ephemeral messages</span>
 </span>
 </th>
 <th width="4%">
 <span class="w3-tooltip">
		<span class="w3-round">FP</span>
		<span style="position:absolute;left:-40px;bottom:36px" class="w3-text w3-tag w3-round w3-large">Foolproof</span>
 </span>
 </th>
 <th width="4%">
 <span class="w3-tooltip">
		<span class="w3-round">DL</span>
		<span style="position:absolute;left:-40px;bottom:36px" class="w3-text w3-tag w3-round w3-large">No data leaks</span>
 </span>
 </th>
 <th width="4%">
 <span class="w3-tooltip">
		<span class="w3-round">DR</span>
		<span style="position:absolute;left:-40px;bottom:36px" class="w3-text w3-tag w3-round w3-large">Data not recoverable</span>
 </span>
 </th>
 <th width="4%">
 <span class="w3-tooltip">
		<span class="w3-round">PFS</span>
		<span style="position:absolute;left:-40px;bottom:36px" class="w3-text w3-tag w3-round w3-large">Perfect Forward Secrecy</span>
 </span>
 </th>
 <th width="4%">Total</th>
 <th width="4%">
 <span class="w3-tooltip">
		<span class="w3-round">ID</span>
		<span style="position:absolute;left:-40px;bottom:36px" class="w3-text w3-tag w3-round w3-large">ID doesn't have personal info</span>
 </span>
 </th>
 <th width="4%">
 <span class="w3-tooltip">
		<span class="w3-round">EP</span>
		<span style="position:absolute;left:-40px;bottom:36px" class="w3-text w3-tag w3-round w3-large">Does not require email/phone</span>
 </span>
 </th>
 <th width="4%">
 <span class="w3-tooltip">
		<span class="w3-round">NT</span>
		<span style="position:absolute;left:-40px;bottom:36px" class="w3-text w3-tag w3-round w3-large">No trackers</span>
 </span>
 </th>
 <th width="4%">Total</th>
 <th width="4%">
 <span class="w3-tooltip">
		<span class="w3-round">Au</span>
		<span style="position:absolute;left:-40px;bottom:36px" class="w3-text w3-tag w3-round w3-large">Audits done</span>
 </span>
 </th>
 <th width="4%">
 <span class="w3-tooltip">
		<span class="w3-round">CV</span>
		<span style="position:absolute;left:-40px;bottom:36px" class="w3-text w3-tag w3-round w3-large">Contact Verification</span>
 </span>
 </th>
 <th width="4%">
 <span class="w3-tooltip">
		<span class="w3-round">GC</span>
		<span style="position:absolute;left:-40px;bottom:36px" class="w3-text w3-tag w3-round w3-large">Good Country</span>
 </span>
 </th>
 <th width="4%">
 <span class="w3-tooltip">
		<span class="w3-round">KC</span>
		<span style="position:absolute;left:-40px;bottom:36px" class="w3-text w3-tag w3-round w3-large">Key Change Alerts</span>
 </span>
 </th>
 <th width="4%">Total</th>
 <th width="4%">
 <span class="w3-tooltip">
		<span class="w3-round">PD</span>
		<span style="position:absolute;left:-40px;bottom:36px" class="w3-text w3-tag w3-round w3-large">P2P or Decentralized</span>
 </span>
 </th>
 <th width="4%">
 <span class="w3-tooltip">
		<span class="w3-round">OS</span>
		<span style="position:absolute;left:-40px;bottom:36px" class="w3-text w3-tag w3-round w3-large">Open Source</span>
 </span>
 </th>
 <th width="4%">
 <span class="w3-tooltip">
		<span class="w3-round">SH</span>
		<span style="position:absolute;left:-40px;bottom:36px" class="w3-text w3-tag w3-round w3-large">Self Hosted</span>
 </span>
 </th>
 <th width="4%">
 <span class="w3-tooltip">
		<span class="w3-round">NP</span>
		<span style="position:absolute;left:-40px;bottom:36px" class="w3-text w3-tag w3-round w3-large">Number of platforms</span>
 </span>
 </th>
 <th width="4%">Total</th>
 </tr>
 
 
{% assign applications = site.data.ratings %}
{% for application in applications %}

{% if application.privacy_message_score == 1 %}
  {% capture message_color %}w3-red{% endcapture %}
{% elsif application.privacy_message_score == 2 %}
  {% capture message_color %}w3-orange{% endcapture %}
{% elsif application.privacy_message_score == 3 %}
  {% capture message_color %}w3-yellow{% endcapture %}
{% elsif application.privacy_message_score == 4 %}
  {% capture message_color %}w3-green{% endcapture %}
{% endif %}

{% if application.privacy_id_score == 1 %}
  {% capture id_color %}w3-red{% endcapture %}
{% elsif application.privacy_id_score == 2 %}
  {% capture id_color %}w3-orange{% endcapture %}
{% elsif application.privacy_id_score == 3 %}
  {% capture id_color %}w3-yellow{% endcapture %}
{% elsif application.privacy_id_score == 4 %}
  {% capture id_color %}w3-green{% endcapture %}
{% endif %}

{% if application.integrity_score == 1 %}
  {% capture integrity_color %}w3-red{% endcapture %}
{% elsif application.integrity_score == 2 %}
  {% capture integrity_color %}w3-orange{% endcapture %}
{% elsif application.integrity_score == 3 %}
  {% capture integrity_color %}w3-yellow{% endcapture %}
{% elsif application.integrity_score == 4 %}
  {% capture integrity_color %}w3-green{% endcapture %}
{% endif %}

{% if application.resistance_score == 1 %}
  {% capture resistance_color %}w3-red{% endcapture %}
{% elsif application.resistance_score == 2 %}
  {% capture resistance_color %}w3-orange{% endcapture %}
{% elsif application.resistance_score == 3 %}
  {% capture resistance_color %}w3-yellow{% endcapture %}
{% elsif application.resistance_score == 4 %}
  {% capture resistance_color %}w3-green{% endcapture %}
{% endif %}

<tr>
 <td class="w3-right-align">{{ application.display_name }}</td>
 <td>{{ application.pm_ephemeral }}</td>
 <td>{{ application.pm_foolproof }}</td>
 <td>{{ application.pm_no_leaks }}</td>
 <td>{{ application.pm_not_recoverable }}</td>
 <td>{{ application.pm_pfs }}</td>
 <td>
   <span class="w3-tooltip">
		 <span class="w3-tag w3-round {{ message_color }} ">{{ application.privacy_message_score }}</span>
   </span>
 </td>
 <td>{{ application.pi_no_info }}</td>
 <td>{{ application.pi_no_ph_em }}</td>
 <td>{{ application.pi_no_trackers }}</td>
 <td>
   <span class="w3-tooltip">
			<span class="w3-tag w3-round {{ id_color }} ">{{ application.privacy_id_score }}</span>
	 </span>
 </td>
 <td>{{ application.i_audits }}</td>
 <td>{{ application.i_cont_ver }}</td>
 <td>{{ application.i_good_country }}</td>
 <td>{{ application.i_key_changes }}</td>
 <td>
   <span class="w3-tooltip">
		 <span class="w3-tag w3-round {{ integrity_color }} ">{{ application.integrity_score }}</span>
	 </span>
 </td>
 <td>{{ application.r_p2p_dec }}</td>
 <td>{{ application.r_opensource }}</td>
 <td>{{ application.r_selfhost }}</td>
 <td>{{ application.r_platforms }}</td>
 <td>
   <span class="w3-tooltip">
		 <span class="w3-tag w3-round {{ resistance_color }} ">{{ application.resistance_score }}</span>
	 </span>
 </td>
</tr>
{% endfor %}
<tr>
  <td>Key to columns:</td>
  <td colspan="6" class="w3-left-align">
    <ul class="w3-small">
    <li>EM - Ephemeral messages</li>
    <li>FP - Foolproof</li>
    <li>DL - No data leaks</li>
    <li>DR - Data not recoverable</li>
    <li>PFS - Perfect Forward Secrecy</li>
    </ul>
  </td>
  <td colspan="4" class="w3-left-align">
  <ul class="w3-small">
  <li>ID - ID doesn't have personal info</li>
<li>EP - Does not require email or phone</li>
<li>NT - No trackers</li>
</ul>
  </td>
  <td colspan="5" class="w3-left-align">
  <ul class="w3-small">
  <li>Au - Audits</li>
<li>CV - Contact Verification</li>
<li>GC - Good Country</li>
<li>KC - Key Change Alerts<br>
(&quot;N/A&quot; means the key cannot change)</li>
  </ul>
  </td>
  <td colspan="5" class="w3-left-align">
  <ul class="w3-small">
  <li>PD - P2P or Decentralized</li>
<li>OS - Open Source</li>
<li>SH - Self Hosted</li>
<li>NP - Number of platforms</li>
</ul>
</td>
</tr>
 </table>



<p>
<h2>Some other apps that are worth considering:</h2>
Notes within [brackets] are potential negative attributes
  <ul>
    <li>{% include generate_app_link.html app_name="wire" %}- [1 tracker, Venture capitalist funding based in USA, not focused on personal use]</li>
    <li>{% include generate_app_link.html app_name="wickrme" %}- [Based in USA, 3 trackers]</li>
    <li>{% include generate_app_link.html app_name="babelnet" %}- Very nice syncing between multiple devices, based outside of the 14 eyes [User interface needs clarified wording, trouble connecting with LineageOS, 1 tracker]</li>
    <li>{% include generate_app_link.html app_name="blabber.im" %}- A fork of Conversations that has a simpler interface</li>
    <li>{% include generate_app_link.html app_name="quicksy" %}- A fork of Conversations that makes it easy to signup, your phone number is used as your ID.</li>
    
  </ul>
Use with caution:<br>
<ul>
    <li>{% include generate_app_link.html app_name="element" %}- [connects to non-encrypted message systems, Based in the UK, no ephemeral messages]</li>
</ul>
  December 2018: Recently there have been some troubling laws passed and articles written in the UK and Australia (part of the <a href="https://restoreprivacy.com/5-eyes-9-eyes-14-eyes/">5 eyes countries</a>) that may cause issues with trust in applications developed in those countries.  Both countries now seem to be pushing for backdoor access for government surveillance to be built into secure messaging applications.  Not only will this weaken or break End to End security, but apps that are not open source from those countries may no longer be trusted and may be used for a mass surveillance program.  Here are some recent articles.<br>
  <a href="https://www.lawfareblog.com/principles-more-informed-exceptional-access-debate">Principles for a More Informed Exceptional Access Debate</a><br>
<div class="w3-panel w3-orange">
  <blockquote>
  In a world of encrypted services, a potential solution could be to go back a few decades. It’s relatively easy for a <u>service provider to silently add a law enforcement participant to a group chat or call</u>. The service provider usually controls the identity system and so really decides who’s who and which devices are involved - they’re usually involved in introducing the parties to a chat or call. You end up with everything still being end-to-end encrypted, but there’s an extra ‘end’ on this particular communication. This sort of solution seems to be no more intrusive than the virtual crocodile clips that our democratically elected representatives and judiciary authorise today in traditional voice intercept solutions and certainly doesn’t give any government power they shouldn’t have.<br>
<br>
We’re not talking about weakening encryption or defeating the end-to-end nature of the service. In a solution like this, we’re normally talking about <u>suppressing a notification on a target’s device</u>, and only on the device of the target and possibly those they communicate with. That’s a very different proposition to discuss and you don’t even have to touch the encryption.<br>
&nbsp;&nbsp;-Ian Levy is the technical director of the National Cyber Security Centre, a part of GCHQ.<br>
&nbsp;&nbsp;-Crispin Robinson is the technical director for cryptanalysis at GCHQ.
</blockquote>
</div>
<br>
  <a href="https://arstechnica.com/tech-policy/2018/12/australia-passes-new-law-to-thwart-strong-encryption/">Australia passes new law to thwart strong encryption</a><br>
  <div class="w3-panel w3-orange">
  <blockquote>
  The new law, which has been pushed for since at least 2017, requires that companies provide a way to get at encrypted communications and data via a warrant process. It also imposes fines of up to A$10 million for companies that do not comply and A$50,000 for individuals who do not comply. In short, the law thwarts (or at least tries to thwart) strong encryption.<br>
<br>
  Companies who receive one of these warrants have the option of either complying with the government or waiting for a court order. However, by default, the orders are secret, so companies would not be able to tell the public that they had received one.
  </blockquote>
  </div>

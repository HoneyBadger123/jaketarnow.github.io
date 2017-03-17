---
layout: post
title: Directed Study - Post 3
description: Device discovery via UDP multicast
image: assets/images/pic01.jpg
---
Currently all of the device discovery via the applications is using ICMP requests. What is the response we get back? As of now, I am sending a network packet and I am looking to see what I get in reply. If something is returned, then it is a known host. Some hosts ignore everything, so how will we get those devics? Try other protocols? Spoof the network?

All of those items are things I am currently asking myself. If there is a known host, we just open a TCP connection and start listening. For devices that can't be found we can try a multicast via UDP. Such devices like Chromecast or Amazon Echo are discoverable via universal plug and play. The idea behind this is that I will multicast an address via a range of IPs. Once I get replies I can open connections between these devices. The entire idea for this application, is if one could execute "arp -a" from their phone. But, its quite difficult and non-secure to execute an arp table in iOS. Especially with Apple's documentation.

Since all of these issue and challenges have been arising, I decided to go back and research some more. I researched again sending raw packets over Swift or Objective-C, and saw a couple of APIs that people have built on GitHub that you could use. The actual Apple Documentation is pretty vague when it comes to networking libraries. I did however fall upon some projects of discovery over UDP and TCP: https://github.com/robbiehanson/CocoaAsyncSocket. I also found an implementation where someone used the SimplePing (https://developer.apple.com/library/content/samplecode/SimplePing/Introduction/Intro.html) from Apple’s Documentation to discover hosts. I set it up in my simulator, and it actually discovered things on my network.
My plan is  to go through the code and try and introduce some of the implementations from the documentation https://github.com/robbiehanson/CocoaAsyncSocket/wiki/Intro_GCDAsyncSocket. If I feel like I am making head-way with this, I think I will stick with the option of building this as an iOS app and use Objective-C instead of Swift. Seems like you have much more freedom and flexibility in regards to Networking with Objective-C.

Next week, I will be testing multicating to IPs for discovery of Bonjour and UPnP devices. 
<div id="disqus_thread"></div>
<script>
/**
* RECOMMENDED CONFIGURATION VARIABLES: EDIT AND UNCOMMENT THE SECTION BELOW TO INSERT DYNAMIC VALUES FROM YOUR PLATFORM OR CMS.
* LEARN WHY DEFINING THESE VARIABLES IS IMPORTANT: https://disqus.com/admin/universalcode/#configuration-variables
*/
/*
var disqus_config = function () {
this.page.url = PAGE_URL; // Replace PAGE_URL with your page's canonical URL variable
this.page.identifier = PAGE_IDENTIFIER; // Replace PAGE_IDENTIFIER with your page's unique identifier variable
};
*/
(function() { // DON'T EDIT BELOW THIS LINE
var d = document, s = d.createElement('script');

s.src = '//jaketarnow.disqus.com/embed.js';

s.setAttribute('data-timestamp', +new Date());
(d.head || d.body).appendChild(s);
})();
</script>
<noscript>Please enable JavaScript to view the <a href="https://disqus.com/?ref_noscript" rel="nofollow">comments powered by Disqus.</a></noscript>

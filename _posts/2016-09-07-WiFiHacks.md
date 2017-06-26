---
layout: post
title: WiFi Hacks
description: Building an app to view devices on a network
image: assets/images/pic04.jpg
---
Over the past week I have been reviewing Apple Developer Guides/Samples on ways to view devices on one's home network via an iOS app, aka Objective-C or Swift.

Through my research I have been able to find sample code on Apple's "Simple Ping". This small application will ping a host until you tell it to stop. I believe this could be utilized in a way to ping a certain range of IP Addresses once the initial one is found.
The only limitation is that via StackOverflow, people have stated that the Objective-C code can only access laptops and desktops, not mobile devices. I am going to be conducting more research into this shortly. 

Another alternative, is to dive into [Apple's Developer Framework](https://developer.apple.com/library/mac/documentation/Networking/Reference/SysConfig/index.html#//apple_ref/doc/uid/TP40001027) and use the System Configuration Framework. 
Using such calls as: SCNetworkInterfaceGetBSDName, we could get a return value of the BSD name associated with the interface or device name. I could also possibly use the SCNetworkProtocolGetEnabled which would display which protocols are enabled, such as HTTP, SMS, FTP, etc..

For the basic speed test that I am thinking about, [Ookla Speedtest](http://www.speedtest.net/mini.php) actually allows you to download their code and use it via PHP, ASP.NET, or JSP. I am thinking that I could convert the PHP code to Objective-C in order to have the speed test available within my app. 

First round design concepts coming soon...

My final proposed solution would be to use a [Raspberry Pi](https://www.raspberrypi.org/forums/viewtopic.php?f=66&t=18207) on the backend as my server. This would act as an inter-mediary between the iOS Application (UI) and all other devices on the network. While running Bonjour on the Raspberry Pi, I could easily discover all devices connected to the same network.
[Bonjour](https://developer.apple.com/bonjour/), also known as zero-configuration networking, enables automatic discovery of devices and services on a local network using industry standard IP protocols. It makes it easy to discover, publish, and resolve network services with an easy-to-use programming interface that is accessable via Cocoa, Ruby, Python and others. 

With all of these in mind and further research and iOS coding over the next week, I should have a definitive route in my stack and application.

Stay tuned!
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

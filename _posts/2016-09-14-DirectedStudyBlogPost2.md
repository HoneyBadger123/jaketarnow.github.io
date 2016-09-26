---
layout: post
title: Directed Study - Post 2
excerpt_separator: <!--more-->
---
For this week we discussed the basic design of the application. As you can see below, the design is quite simple right now. My plan is to allow the user to select the Wifi network that they wish to scan. Once slected, they can choose between a speed tests or device discovery. <!--more-->
The application will use ICMP protocols for device discovery. Yet, we will probably investigate other protocols as some things such as an Amazon Echo are hard to discover from a basic brute force ICMP pinging technique.
![Snoopy App V1]({{ site.url }}/images/Screen Shot 2016-09-15 at 8.26.53 PM.png =200x300){: .center-image }
I was able to prototype some code via Swift to display the SSID and BSSID on the application. Yet, after researching more into Swift, I realized that are many limitations when it comes to networking and socket programming. I have since migrated over to Objective-C, where I can use more libraries and execute raw C code. Hopefully this works well and can help me accomplish the tasks that I have set for this application.

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

---
layout: post
title: Directed Study - Post X
description: Finishing the project
image: assets/images/pic01.jpg
---
Well, it's been a while. Super focused on all my projects and keep getting hit with issues and blocks on this one. Since my last post...which was about a month ago, we now have ICMP discovery and UPNP discovery working. *For anyone ever using C code within Objective-C...please please please be aware of you address space and how much memory you are allocating. Running C from cmd line is so much nicer with gdb and flags then in XCode*. 

In the main app's table, you will see all devices that are found and the discovery protocol used. If you would like to run diagnostics for such device, you can click on a button where a nice little pop-up displays it.

But, there is no speedtest currently. *:(* I was able to research a pretty simple and efficient speedtest script that is using Python and C. Yet, there is not a ton of documentation on how to execute Python from Objective-C. So on we go, digging through StackOverflow and testing out scripts from terminal. 

Currently digging through all of that to try and find some hope! As well as accomplishing the speedtest, I have also been researching persistent storage within iOS. If I use a specific class called the *NSUserDefaults* class, then I can store app-specific preferences in a property list and all file handling is encapsulated by this class. With all of this, there is a synchronize method that writes changes to the file, so when your app terminates everything is saved. 

From all of this, I was able to create an archive and unarchive function, that writes the data (discovered devices) to your archive.dat file on your device. Then, upon re-opening the device it will pull this data back into the app. This can serve as a nice way of persistent storage for re-opening your app, and it can be used to run statistical models on how often said device is found upon discovery.

Only got two more weeks to finish this application...wish me luck!
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

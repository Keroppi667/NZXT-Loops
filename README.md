This repository is for ppl with NZXT Kraken AIO coolers that "support" Web integration within their CAM software.

This repo only exists because NZXT sucks so badly that they can't be bothered to include basic things, like allowing you to insert a replacement video for their (worthless) Youtube connector and (even at most basic) allowing it to save a different video per profile.

You'll find that the only way playing a YT video works correctly is: by replacing their video *for adverstising the product you have already bought* in their pre-made YT "profile" in the CAM software. Yeah...they're very stable geniuses. 
You'll also find that even if you save/change profiles, the URL setting follows. So: you get ONE video slot, total. No searching in %appdata%/NZXT/ to modify config files will help you.
Evidently these assholes never heard of (or thought to) include a simple copy or add button.

If you've tried working around this, you'll find that just putting in a web link to a Youtube video under "Web Integrations" DOES produce a result, but it's effectively letterboxed garbage. 
No amount of URL parameters will change that. To get it to work, NZXT proxied it to a specifically formatted HTML "page" (iframe) that shows the youtube video.

So, if you were (also) a sucker and spent nearly $300 on an AIO (with completely half-baked software), and you *just want to display a youtube video in full screen on your little AIO* ...tough titties!

After 2 hours of my life wasted, I realized/accepted there was no other options than: replicating the way they did it. Which means pointing the integration at their custom iframe page.
At least: they posted their template to build a "custom" connector. Evidently, "custom" also means replicating the in-built functionality too.

In each folder in this repo: there is a simple index.html that really does fuck all other than link to the video and spit it out into a specifically sized iframe. You'll need to make a file for EACH of the videos you want on your LCD as "Web Integrations". 
Yeah, you gotta make a fucking HTML file for every YT video you want to display in excess of the single slot they pre-setup for you. Thanks, NZXT.

Use mine as-is or make your own.

INSTRUCTIONS:
1. Copy the contents of any index.html to your own repo. (Wherever you put it, name it index.html)

    If you haven't ever set up Github pages (required for regular display/publishing of things like webpages like a normal webserver displays them) go to:
    (Your Repo)>'Settings' (in top bar)>'Pages' and make sure to set your source ('Deploy from a branch'>(Repo))

2. Edit the Youtube video ID and optionally add any relevant URL parameters (like start time) toward the bottom of the file, and save.

3. Get your integration URL. Your "Web Integration" URL will be:
4. 
    https://(username).github.io/(path-to-index.html)
   
    NOT
   
    https://github.com/(username)/(path-to-index.html)
    
    Notice the difference in both username placement and *.io vs *.com in the domain.
    
    So, for:
    https://github.com/Keroppi667/NZXT-Loops/eyes/
   
    the URL will become:
   
    https://keroppi667.github.io/NZXT-Loops/eyes/

5. Add this URL in the "Web Integration" section of the NZXT CAM software

6. Join me in wishing "a pox on all their houses" for the devs that can overlook such simple and criitical functionality like a copy or add button.

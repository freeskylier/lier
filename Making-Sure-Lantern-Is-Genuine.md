Malicious actors may try to impersonate official Lantern web pages, software, email, and more to spread false information, track potential Lantern users, or (worse) spread [malware](https://en.wikipedia.org/wiki/Malware) disguised as Lantern. **It is very important to always make sure Lantern content is genuine.**

Fortunately, verifying that Lantern content is genuine is relatively simple. See below to find out how, but first, **here is how you can tell that this page is itself genuine:** Look at the address bar in your browser and note that the address begins with exactly the following: `https://github.com/getlantern`. This is the official home of the Lantern project on github.com, which is the site used to host Lantern's source code and documentation. **(TODO: Update this when we migrate the docs off the GitHub wiki.)**

With that out of the way, read on to find out how to verify other sources of Lantern content.

## getlantern.org

The official Lantern web site is [https://getlantern.org](https://getlantern.org). Notice the *https* (as opposed to *http*) in the beginning of that address. **Always using the https address means your browser will guarantee it's talking to the official getlantern.org web site.** If anyone with the ability to intercept and tamper with your traffic (such as your government or ISP) tried to do so, using https means your browser can detect this and warn you about it rather than loading the phony site.[1]

Also notice that "getlantern.org" looks a lot like "getIantern.org" (with a capital "i" in place of the lowercase "l") and also looks a lot like "getlantem.org" (with an "m" in place of the "rn"), especially with certain fonts. Team Lantern has bought up all these lookalike domains (as well as registered the lookalike usernames on GitHub, Twitter, etc.) to make sure no one can use them to trick people.

## getlantern.org Official Mirror

The getlantern.org web site is blocked in certain countries, but Amazon S3 -- a widely used web hosting provider -- is often unblocked in these countries. For this reason, the Lantern developers maintain an official mirror of getlantern.org on S3 at the following address:

https://s3-ap-southeast-1.amazonaws.com/getlantern/ (note the "https" here as well)

**This is the one and only official mirror of getlantern.org.** If you ever see a web site claiming to be Lantern that is neither https://getlantern.org nor the official mirror above, **don't trust it.**

## Official Lantern Email

TODO

## Official Lantern Software

TODO

## Other Official Lantern Accounts

- https://twitter.com/getlantern
- https://www.facebook.com/getlantern
- https://www.youtube.com/getlantern
- http://get-lantern.tumblr.com/
- http://lanterndev.tumblr.com/

[1] Advanced users who wish to verify getlantern.org's https certificate can check that its SHA1 matches the following fingerprint: DE 5F B1 45 AE 9A D3 15 30 D7 DB AF 85 91 C7 A8 62 F5 15 D3. See https://www.grc.com/fingerprints.htm for third-party verification.
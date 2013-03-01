Debugging the many complex layers of proxying in Lantern can often get confusing. That combined with browser and OS-specific oddities with proxies can be enough to make a developer's head spin! Here are some frequently encountered issues and how to diagnose them -- this list will grow over time.

* Chrome stops using a proxy when it thinks it's bad. Check out chrome://net-internals/proxyservice.config#proxy to see if this is the case and reset it if it is. Lantern can get on the list if you're working on proxying code and break it, for example, or if a CTRL-C bypasses the shutdown handler and results in the unproxy code not getting called, or if the unproxy code does get called but after the Lantern proxy is shut down. You get the idea!

 
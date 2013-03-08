Debugging the many complex layers of proxying in Lantern can often get confusing. That combined with browser and OS-specific oddities with proxies can be enough to make a developer's head spin! Here are some frequently encountered issues and how to diagnose them -- this list will grow over time.

* Chrome stops using a proxy when it thinks it's bad. Check out chrome://net-internals/proxyservice.config#proxy to see if this is the case and reset it if it is. Lantern can get on the list if you're working on proxying code and break it, for example, or if a CTRL-C bypasses the shutdown handler and results in the unproxy code not getting called, or if the unproxy code does get called but after the Lantern proxy is shut down. You get the idea!

* The Lantern UI is rendered inside a standalone instance of Google Chrome. As such, the Google Chrome developer tools are available and are an essential debugging tool. (See https://developers.google.com/chrome-developer-tools/docs/console for a guide to their usage.)

    * To enable debug logging to the Javascript console (disabled when running from a release version), set the config.dev flag to true in [app.js](https://github.com/getlantern/lantern-ui/blob/master/app/js/app.js).

    * Setting `logLevel: 'debug'` in the cometdSrvc configuration in [services.js](https://github.com/getlantern/lantern-ui/blob/master/app/js/services.js) can also help debug issues with cometd. In dev mode, the model object is published to the `window` global, so you can easily inspect the model from the console. You can also make local changes to the model by modifying fields on `model`.

    * The [AngularJS Batarang](https://github.com/angular/angularjs-batarang) can also be extremely useful for debugging Angular apps. And of course, the [AngularJS Docs](http://docs.angularjs.org/guide/) are an essential resource for understanding how AngularJS apps work.
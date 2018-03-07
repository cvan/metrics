# WebXR Metrics

Help improve the [WebXR](https://immersive-web.github.io/webxr/) API ecosystem and community by sending usage statistics, performance metrics, and JavaScript errors to the [Mozilla Mixed Reality](https://vr.mozilla.org/) team.


## Telemetry Usage

To opt in to telemetry (i.e., collecting usage statistics, performance metrics, and catching errors)  it in your WebXR site, simply include this snippet of JavaScript code in your HTML (ideally, immediately before the `</head>` or before `</body>`):

```html
<script src="https://webxr.services/metrics.js" async defer></script>
```

Or this:

```html
<script>
  // Telemetry for collecting basic usage statistics, performance metrics, and catching errors.
  (function () {
    function injectScript () {
      if (!navigator.onLine) {
        return;
      }
      var refScript = document.querySelector('script');
      var script = document.createElement('script');
      script.src = 'https://webxr.services/metrics.js';
      script.async = true;
      script.crossorigin = 'anonymous';
      (refScript ? refScript.parentNode : document.head).insertBefore(script, ref);
    }
    injectScript();
    window.addEventListener('online', injectScript);
  })();
</script>
````

We  [telemetry metrics][TELEMETRY.MD], if your site has a [W3C Web-App Manifest](https://w3c.github.io/manifest/) included (referenced by `<link rel="manifest" href="manifest.webmanifest">` in the HTML of your site), the WebXR Agent displays a navigation bar at the bottom of your page, rendering the metadata for your app (including its logo, name, description), detecting the user's connected VR headsets, as well as managing entering/exiting VR mode, including mechanisms for streamlined page-to-page (i.e., scene-to-scene) navigation. (Easter egg: check out the keyboard shortcuts. _Hint: you can talk your computer, and it'll talk back._)

The library's [open-source code is on GitHub](https://github.com/MozillaReality/webxr-agent), released under the [Creative Commons CC0-1.0 Public Domain license](https://github.com/MozillaReality/webxr-agent#license). We welcome your contributions!

Below you can enjoy some example scenes adapted from [Erica Layton](https://twitter.com/EricaLayton)'s magical [SkyIslands VR](https://www.skyislandsvr.com/) worlds (each site with its own web-app manifest and embedded `<script>` tags for the WebXR Agent).<br><br>


## Demo usage

### [Carnival Globe Trees](https://skyislands.webvr.rocks/carnivalglobetrees.html)

<a href="https://skyislands.webvr.rocks/carnivalglobetrees.html"><img src="https://cloud.headwayapp.co/changelogs_images/images/big/000/003/462-18f144dddc0c060cecc0de7d7ac4de696d363293.png" alt="Screenshot of SkyIslands VR: Carnival Globe Trees (embedded WebXR Agent, with a web-app manifest)" title="SkyIslands VR: Carnival Globe Trees" width="400"></a>

<details>
  <ul>
    <li>
      <strong><a href="https://skyislands.webvr.rocks/carnivalglobetrees.html">View the WebVR site</a></strong>
      <ul>
        <li>
          <a href="https://github.com/WebVRRocks/skyislands/blob/master/carnivalglobetrees.webmanifest">View the source code</a>
        </li>
      </ul>
    </li>
    <li>
      <strong><a href="https://fetchmanifest.org/manifest?ws=2&url=https://skyislands.webvr.rocks/carnivalglobetrees.html">View the processed manifest</a></strong>
      <ul>
        <li>
          <a href="https://github.com/WebVRRocks/skyislands/blob/master/carnivalglobetrees.webmanifest">View the source code</a>
        </li>
      </ul>
    </li>
  </ul>
</details>

<hr>

### [Dark Lotus](https://skyislands.webvr.rocks/darklotus.html)

<a href="https://skyislands.webvr.rocks/darklotus.html"><img src="https://cloud.headwayapp.co/changelogs_images/images/big/000/003/463-40cf0fe3146f7722f9fc57b0e5a5e9d3e61845fe.png" alt="Screenshot of SkyIslands VR: Dark Lotus (embedded WebXR Agent, with a web-app manifest)" title="SkyIslands VR: Dark Lotus" width="400"></a>

<details>
  <ul>
    <li>
      <strong><a href="https://skyislands.webvr.rocks/darklotus.html">View the WebVR site</a></strong>
      <ul>
        <li>
          <a href="https://github.com/WebVRRocks/skyislands/blob/master/darklotus.webmanifest">View the source code</a>
        </li>
      </ul>
    </li>
    <li>
    <strong><a href="https://fetchmanifest.org/manifest?ws=2&amp;url=https://skyislands.webvr.rocks/darklotus.html">View the processed manifest</a></strong>
    <ul>
      <li>
        <a href="https://github.com/WebVRRocks/skyislands/blob/master/darklotus.webmanifest">View the source code</a>
      </li>
    </ul>
    </li>
  </ul>
</details>

<hr>

### [Meditation Orbs](https://skyislands.webvr.rocks/meditationorbs.html)

<a href="https://skyislands.webvr.rocks/meditationorbs.html"><img src="https://cloud.headwayapp.co/changelogs_images/images/big/000/003/465-de99f33a494a725593c5df92fdf10c1a2bf85b03.png" alt="Screenshot of SkyIslands VR: Meditation Orbs (embedded WebXR Agent, with a web-app manifest)" title="SkyIslands VR: Meditation Orbs" width="400"></a>

<details>
  <ul>
    <li>
      <strong><a href="https://skyislands.webvr.rocks/meditationorbs.html">View the WebVR site</a></strong>
      <ul>
        <li>
          <a href="https://github.com/WebVRRocks/skyislands/blob/master/meditationorbs.webmanifest">View the source code</a>
        </li>
      </ul>
    </li>
    <li>
      <strong><a href="https://fetchmanifest.org/manifest?ws=2&amp;url=https://skyislands.webvr.rocks/darklotus.html">View the processed manifest</a></strong>
      <ul>
        <li>
          <a href="https://github.com/WebVRRocks/skyislands/blob/master/meditationorbs.webmanifest">View the source code</a>
        </li>
      </ul>
    </li>
  </ul>
</details>

<hr>

If you have any issues or feature requests, feel free to [file an issue](https://github.com/MozillaReality/webxr-agent/issues) on the [GitHub project](https://github.com/MozillaReality/webxr-agent). Also, don't hesitate to [contact](https://twitter.com/cvanw) [us](https://twitter.com/whoyee) if there are any fun WebVR scenes in the wild that you'd like use the WebXR Agent.

<hr>


## Local development

First, clone this repo:

```sh
git clone git@github.com:MozillaReality/metrics.git metrics && cd metrics
```

To install the [Node.js](https://nodejs.org/en/download/) dependencies:

```sh
npm install
```

To start the local development server:

```sh
npm start
```


## Deployment

This project is automatically deployed to [GitHub Pages](https://webvr.services/metrics.js) when commits land on the `master` branch of this repository.


## License

Copyright 2017 - 2018 Mozilla Corporation.

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.

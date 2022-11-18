# GSoC 2021 Report - Apertium Webext

Or more appropriately, a report of the work I've done on it. This gist is the Work Product Submission for the progress on [my GSoC'21 Project](https://summerofcode.withgoogle.com/projects/#4924808795521024), Apertium Webext. The project was completed in 3 months, from June to August of 2021 and mentored by [Tino Didriksen](https://github.com/TinoDidriksen).

<br>

### Important Links

- [The Actual Repository](https://github.com/apertium/apertium-webext)
- [Log of all my commits](https://apertium.projectjj.com/gsoc2021/OverPoweredDev.html)
- [Its Wiki Page](https://wiki.apertium.org/wiki/Apertium_Webext)
- [My Original GSoC Proposal](https://wiki.apertium.org/wiki/User:OverPowered/GSoC2021Proposal)
- [And its Progress Report](https://wiki.apertium.org/wiki/User:OverPowered/GSoC2021_Progress_Report)
- [Who am I?](https://github.com/OverPoweredDev)

<br>

### Progress Checklist

- [x] Create an extension
  - [x] Extension has required elements: pop-up, background page, content scripts and the settings page
  - [x] Extension must work across browsers (yay Chromium!)
- [x] Add Translation Features to the extension
  - [x] Translate between an existing language pair in the extension pop-up
  - [x] Translate a word or phrase that the user hovers on on a website
  - [x] Add Contextual Translation as well for hover-on gists
  - [x] Translate an entire webpage at a time
- [x] Enable settings for the user
  - [x] Create a settings page accessible from the extension menu
  - [x] Add an option to select the default translate-to language
  - [x] Allow switching of the Apertium Source (Release/Beta/Local)
  - [x] Allow Editing of the website list for default hover-on gists
- [x] Implement tests for the extension
- [ ] Automate testing on any commit/push
- [ ] Publish the Extension on Firefox's Add-On store
- [ ] Enable support for Firefox Android/Safari

<br>

### Summary of the Project

Apertium Webext is a browser extension designed as a front-end for the Apertium Apy Service. It's main tasks, as outlined in the initial Proposal are: 
1. Translation of Words/Phrases given in the extension Pop-up
2. Translation of Words the user hovers on
3. Translation of Words/Phrases hovered on, but also with context
4. And finally, translation of the entire webpage

In the development of this project, I've used various tools such as [jQuery](https://jquery.com/) and [Bootstrap](https://getbootstrap.com/) for front-end development and [Puppeteer](https://pptr.dev/) along with [Mocha](https://mochajs.org/) for testing. The details of the manifest, file structure and all can be found on the [official repository](https://github.com/apertium/apertium-webext).

Even with all these, my work isn't complete. A few goals that are yet to be complete are publishing the extension on the Firefox Add-On store as well as a version for Safari. Apart from these, there's a few minor upgrades I plan on doing soon.

<br>

### My Experiences

From the initial proposal through the community bonding period and in these final few days, it's honestly been a pleasure working on this project. I was somewhat doubtful about some features when I was starting out, worried about not being able to finish it in time. Thankfully, it's all worked out great by the end.

The most challenging parts (at least for me) were the lack of tools dealing with extensions. Mozilla's [webext-polyfill](https://github.com/mozilla/webextension-polyfill) lacks a couple features, especially Context Menus, in making a completely cross-platform extension. Even when testing, Puppeteer is one of the few tools available for extensions (Selenium works too but Puppeteer works right out the box).

Another feature that I needed help with was extracting the right parts from the DOM without including their children, the inner html, certain tags and only the text nodes. My Apertium Mentor, Tino Didriksen helped out big time with [this section](https://github.com/apertium/apertium-webext/blob/a39167dd7180f989c57f6323f21a2b26d9b005d0/src/lib/translate.js#L136).

A more detailed (and less flowery) version of my progress throughout these 10 weeks is available [right here](https://wiki.apertium.org/wiki/User:OverPowered/GSoC2021_Progress_Report).

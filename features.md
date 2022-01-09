---
title: Features
description:
---

*This section overviews the features of ungoogled-chromium. For more detailed information, it is best to consult the source code.*

Contents of this section:

* [Key Features](#key-features)
* [Enhancing Features](#enhancing-features)
* [Borrowed Features](#borrowed-features)
* [Supported Platforms and Distributions](#supported-platforms-and-distributions)

### Key Features

*These are the core features introduced by ungoogled-chromium.*

* Disable functionality specific to Google domains (e.g. Google Host Detector, Google URL Tracker, Google Cloud Messaging, Google Hotwording, etc.)
    * This includes disabling [Safe Browsing](//en.wikipedia.org/wiki/Google_Safe_Browsing). Consult [the FAQ for the rationale](//ungoogled-software.github.io/ungoogled-chromium-wiki/faq#why-is-safe-browsing-disabled).
* Block internal requests to Google at runtime. This feature is a fail-safe measure for the above, in case Google changes or introduces new components that our patches do not disable. This feature is implemented by replacing many Google web domains in the source code with non-existent alternatives ending in `qjz9zk` (known as domain substitution; [see docs/design.md](docs/design.md#source-file-processors) for details), then [modifying Chromium to block its own requests with such domains](patches/core/ungoogled-chromium/block-trk-and-subdomains.patch). In other words, no connections are attempted to the `qjz9zk` domain.
* Strip binaries from the source code (known as binary pruning; [see docs/design.md](docs/design.md#source-file-processors) for details)

### Enhancing Features

*These are the non-essential features introduced by ungoogled-chromium.*

* Add many new command-line switches and `chrome://flags` entries to configure new features (which are disabled by default). See [docs/flags.md](docs/flags.md) for the exhaustive list.
* Add *Suggestions URL* text field in the search engine editor (`chrome://settings/searchEngines`) for customizing search engine suggestions.
* Add more URL schemes allowed to save page schemes.
* Add Omnibox search provider "No Search" to allow disabling of searching
* Add a custom cross-platform build configuration and packaging wrapper for Chromium. It currently supports many Linux distributions, macOS, and Windows. (See [docs/design.md](docs/design.md) for details on the system.)
* Force all pop-ups into tabs
* Disable automatic formatting of URLs in Omnibox (e.g. stripping `http://`, hiding certain parameters)
* Disable intranet redirect detector (extraneous DNS requests)
    * This breaks captive portal detection, but captive portals still work.
* (Iridium Browser feature change) Prevent URLs with the `trk:` scheme from connecting to the Internet
    * Also prevents any URLs with the top-level domain `qjz9zk` (as used in domain substitution) from attempting a connection.
* (Windows-specific) Do not set the Zone Identifier on downloaded files

### Borrowed Features

In addition to the features introduced by ungoogled-chromium, ungoogled-chromium selectively borrows many features from the following projects (in approximate order of significance):

* [Inox patchset](//github.com/gcarq/inox-patchset)
* [Bromite](//github.com/bromite/bromite)
* [Debian](//tracker.debian.org/pkg/chromium-browser)
* [Iridium Browser](//iridiumbrowser.de/)

### Supported Platforms and Distributions

[See docs/platforms.md for a list of supported platforms](//github.com/Eloston/ungoogled-chromium/blob/master/docs/platforms.md).

Other platforms are discussed and tracked in this repository's Issue Tracker. Learn more about using the Issue Tracker [in the Support page](//github.com/Eloston/ungoogled-chromium/blob/master/SUPPORT.md).

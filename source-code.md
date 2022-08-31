---
title: Source Code
description:
---

[The main ungoogled-chromium repository](//github.com/ungoogled-software/ungoogled-chromium) only contains the common code for all platforms; it does not contain all the configuration and scripts necessary to build ungoogled-chromium. Most users will want to use platform-specific repos, where all the remaining configuration and scripts are provided for specific platforms:

[**Find the repo for a specific platform here**](//github.com/ungoogled-software/ungoogled-chromium/blob/master/docs/platforms.md).

If you wish to include ungoogled-chromium code in your own build process, consider using [the tags of the main repo](//github.com/ungoogled-software/ungoogled-chromium/tags). These tags follow the format `{chromium_version}-{revision}` where

* `chromium_version` is the version of Chromium used in `x.x.x.x` format, and
* `revision` is a number indicating the version of ungoogled-chromium for the corresponding Chromium version.

Additionally, most platform-specific repos extend their tag scheme upon this one.

**Building the source code**: [See docs/building.md](//github.com/ungoogled-software/ungoogled-chromium/blob/master/docs/building.md)

---
title: About ungoogled-chromium
description: A brief overview
---

**ungoogled-chromium is Google Chromium**, sans dependency on Google web services. It also features some tweaks to enhance privacy, control, and transparency *(almost all of which require manual activation or enabling)*.

**ungoogled-chromium retains the default Chromium experience as closely as possible**. Unlike other Chromium forks that have their own visions of a web browser, ungoogled-chromium is essentially a drop-in replacement for Chromium.

**Help is always welcome!** See the [docs/contributing.md](//github.com/ungoogled-software/ungoogled-chromium/blob/master/docs/contributing.md) document for more information.

## Motivation and Philosophy

Without signing in to a Google Account, Chromium does pretty well in terms of security and privacy. However, Chromium still has some dependency on Google web services and binaries. In addition, Google designed Chromium to be easy and intuitive for users, which means they compromise on transparency and control of inner operations.

ungoogled-chromium addresses these issues in the following ways:

1. Remove all remaining background requests to any web services while building and running the browser
2. Remove all code specific to Google web services
3. Remove all uses of pre-made binaries from the source code, and replace them with user-provided alternatives when possible.
4. Disable features that inhibit control and transparency, and add or modify features that promote them (these changes will almost always require manual activation or enabling).

These features are implemented as configuration flags, patches, and custom scripts. For more details, consult the [Design Documentation](//github.com/ungoogled-software/ungoogled-chromium/blob/master/docs/design.md).

<!--
<ul class="staff">
	{% for person in site.staff_members %}
		<li>
			<div class="square-image"><img src="{% include relative-src.html src=person.image_path %}" alt="{{ person.name }}"/></div>
			<div class="name"><a target="_blank" href="https://github.com/{{ person.github }}">{{ person.name }}</a></div>
			<div class="position">{{ person.position }}</div>
		</li>
	{% endfor %}
</ul
-->

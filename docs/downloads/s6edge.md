---
layout: default
title: "Downloads for Samsung Galaxy S6 Edge"
---

{% assign device = page.name | remove: '.md' %}
{% assign devicedata = site.data[device] %}
[ <-- Back](/)

# {{ page.title }}
- {: #extraspace} [LineageOS 20 (Android 13)]({{ devicedata.latest_los200 }}){: #dl}
<br>
XDA Thread: [here]({{ devicedata.xda_los200 }})
<br>
Changelog and history: [here](/changelog/lineage20/{{ device }})
<br>
Screenshots: [here](/screenshots/lineage20/universal7420/screenshots)
- {: #extraspace}[LineageOS 19.1 (Android 12.1)]({{ devicedata.latest_los191 }}){: #dl}
<br>
XDA Thread: [here]({{ devicedata.xda_los191 }})
<br>
Changelog and history: [here](/changelog/lineage19/{{ device }})
<br>
Screenshots: [here]()

{% include disclaimer.md %}

{% include compatability.md %}

{% include install.md %}

{% include sourcecode.md %}
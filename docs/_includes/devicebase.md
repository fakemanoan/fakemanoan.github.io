{% assign device = page.name | remove: '.md' %}
{% assign devicedata = site.data[device] %}
[ <-- Back](/)

# {{ page.title }}

{% if devicedata.latest_los200 %}
- {: #extraspace} [LineageOS 20 (Android 13)]({{ devicedata.latest_los200 }}){: #dl}
<br>
XDA Thread: [here]({{ devicedata.xda_los200 }})
<br>
Changelog and history: [here](/changelog/lineage20/{{ device }})
<br>
Screenshots: [here](/screenshots/lineage20/universal7420/screenshots)
{% endif %}
{% if devicedata.latest_los191 %}
- {: #extraspace} [LineageOS 19.1 (Android 12.1)]({{ devicedata.latest_los191 }}){: #dl}
<br>
XDA Thread: [here]({{ devicedata.xda_los191 }})
<br>
Changelog and history: [here](/changelog/lineage19/{{ device }})
<br>
Screenshots: [here](/screenshots/lineage19/universal7420/screenshots)
{% endif %}
{% if device == "s6" || device == "s6edge" %}
# IMPORTANT INFO - READ 
**If you have a SIM lock, please flash the following appropriate builds and remove SIM lock in Settings. There is currently a bug that prevents SIM locks from working properly on these devices.**

Android 12:
<https://github.com/fakemanoan/LineageOS-Releases/releases/tag/A12L-20022024>  
Android 13:
<https://github.com/fakemanoan/LineageOS-Releases/releases/tag/A13-19012024>

{% endif %}

<br><br>

{% include disclaimer.md %}

{% include compatability.md %}

{% include install.md %}

{% include sourcecode.md %}
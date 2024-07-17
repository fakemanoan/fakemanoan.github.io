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
**If you have a SIM security lock, remove the SIM lock prior to flashing. There is currently a bug that prevents SIM cards from working when you have a SIM lock enabled**

Reflash stock software, or use another phone, and remove the SIM lock. 

----------------------------------------------------------------------------

{% endif %}

{% include disclaimer.md %}

{% include compatability.md %}

{% include install.md %}

{% include sourcecode.md %}
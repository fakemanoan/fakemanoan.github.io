{% assign devdownloads = devicedata.downloads %}

## Before installing, some things to note

- VoLTE and WiFi calling are not available currently
{%- if device == "s6" || device == "s6edge" -%}
<br>
- If you have a SIM security lock (entering a PIN before you gain network access), remove it prior to installation. Otherwise you will not have network access
{%- endif -%}
<br>
- My ROMs have KernelSU built in. Read more [here](/kernelsu)
- Check compatability below, and download the correct version for your device
- Follow the install guide at the bottom of the page, NOT OTHERS ON THE INTERNET.
- My ROMs are just LineageOS. They are not explicitly "de-googled" or "privacy" focused. If your device came with my ROM preinstalled, you were likely scammed.
{% include compatability.md %}

{% for dltypes in devicedata.dltypes %}
# {{ devicedata.formalname }} ({{ dltypes.friendly }})
{% for iden in devdownloads %}
{% if iden.type == dltypes.type %} 
- {: #extraspace} [{{ iden.version }}]({{ iden.latest }}){: #dl} <br>
XDA Thread: [here]({{ iden.xda }}) <br>
Changelog and history: [here](/changelog/{{ iden.version | replace: ' ', '' | split: '.' | first | slugify: "ascii" }}/{{ device }}) <br>
Screenshots: [here](/screenshots/{{ iden.version | replace: ' ', '' | split: '.' | first | slugify: "ascii" }}/universal7420/screenshots) <br>
{% endif %}  
{% endfor %}

{% endfor %}


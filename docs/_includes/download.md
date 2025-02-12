{% assign devdownloads = devicedata.downloads %}

## Before installing, some things to note

- VoLTE and WiFi calling are not available on any Samsung phone with LineageOS
{%- if device == "s6" || device == "s6edge" -%}
- If you have a SIM security lock (entering a PIN before you gain network access), remove it prior to installation. Otherwise you will not have network access
{% endif %}
- Check device compatability below, and download the correct version for your device.
- Follow the install guide at the bottom of the page, NOT OTHERS ON THE INTERNET.

{% include compatability.md %}

{% for dltypes in devicedata.dltypes %}
# {{ devicedata.formalname }} ({{ dltypes.friendly }})
{% for iden in devdownloads %}
{% if iden.type == dltypes.type %} 
- {: #extraspace} [{{ iden.version }}]({{ iden.latest }}){: #dl} <br>
XDA Thread: [here]({{ iden.xda }}) <br>
Changelog and history: [here](/changelog/lineage20/{{ device }}) <br>
Screenshots: [here](/screenshots/lineage20/universal7420/screenshots) <br>
{% endif %}  
{% endfor %}

{% endfor %}


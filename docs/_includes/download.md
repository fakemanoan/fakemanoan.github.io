{% assign devdownloads = devicedata.downloads %}

{% include compatability.md %}

Install guide is at the bottom of the page.

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

{% if device == "s6" || device == "s6edge" %}
# IMPORTANT INFO - READ 
**If you have a SIM security lock, remove the SIM lock prior to flashing. There is currently a bug that prevents SIM cards from working when you have a SIM lock enabled**

Reflash stock software, or use another phone, and remove the SIM lock. 

----------------------------------------------------------------------------

{% endif %}

{% assign device = page.name | remove: '.md' %}
{% assign devicedata = site.data[device] %}
[ <-- Back](/)

# {{ page.title }}

{% include download.md %}

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
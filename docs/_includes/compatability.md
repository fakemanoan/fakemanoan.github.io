{% assign devicemodels = devicedata.models %}

# Supported devices
Not all devices are the same. Some use different screens, modems, or other parts. This can mean they are incompatible.

Please download the correct version for your device to ensure correct operation. Unsupported phones will not work.
<table>
<thead><tr><th>Model</th><th>Codename</th><th>Supported</th></tr></thead>
{% for iden in devicemodels %}
<tr><td>{{ iden.iden }}</td><td>{{ iden.codename }}</td><td>
{% if iden.dltype != null %} ✅ 
{% for iden2 in devicedata.dltypes %}
{% if iden2.type == iden.dltype %}
{{ iden2.friendly }}
{% endif %}
{% endfor %}
{% else %} 
❌ 
{% endif %}
</td></tr>
{% endfor %}
</table>

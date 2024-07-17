{% assign devicemodels = devicedata.models %}

# Supported devices
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

Not all devices are created equal. Some models use different parts, which are currently incompatible. 

If your phone is unsupported, you won't be able to install it on your device.
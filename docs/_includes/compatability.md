{% assign devicemodels = devicedata.models %}

# Supported devices
Not every device is created the same. Some phones use different parts internally. This makes them incompatible.

This means if your phone isn't supported, you shouldn't install it on your device.

Make sure you install the correct version, or you may run into issues.
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

{% assign devicemodels = devicedata.models %}

# Supported devices
<table>
<thead><tr><th>Model</th><th>Codename</th><th>Supported</th></tr></thead>
{% for iden in devicemodels %}
<tr><td>{{ iden.iden }}</td><td>{{ iden.codename }}</td><td>{% if iden.supported %} ✅ {% else %} ❌ {% endif %}</td></tr>
{% endfor %}
</table>

I would like to support all devices, however certain bugs or quirks causes basic functions to misbehave or not work properly. While these bugs or quirks exist, these will be unsupported.
{% assign devicemodels = devicedata.models %}

# Supported devices
Despite using the same name, not all device models use the same parts, so they may not be compatible.

Download the corresponding version for your device. If your phone isn't listed it probably isn't supported
<table>
<thead>
<tr>
<th>Model</th> <th>Codename</th> <th>Supported</th></tr>
</thead>

{% for iden in devicemodels %}
<tr>
<td>{{ iden.iden }}</td> <td>{{ iden.codename }}</td> 

<td>
{% if iden.dltype != null %} ✅ 
{% assign split = iden.dltype | split: "+" %}
{% for friendlies in split %}
{% assign temp = friendlies | plus: 0 %}
{{  devicedata.dltypes[temp].friendly }}
{% endfor %}
{% else %} 
❌ 
{% endif %}
</td>
</tr>
{% endfor %}
</table>

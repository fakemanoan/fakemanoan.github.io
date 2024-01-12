---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: "Lineage 20 Screenshots"
---

# Screenshots

<h1> 
{% for image in site.static_files %}
    {% if image.path contains '/assets/img/screenshots/lineage20' %}
        <img src="{{ image.path }}" style="box-shadow: 0px 0px 0px 1px;"> <br> <br>
    {% endif %}
{% endfor %}
</h1>
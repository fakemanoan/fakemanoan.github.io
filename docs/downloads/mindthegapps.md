---
layout: default
title: "Downloads for MindTheGapps Legacy"
---
[ <-- Back](../../)

{% assign gapps = site.data.mindthegapps %}

# About MindTheGapps Legacy
MindTheGapps legacy is a modified version of MindTheGapps which will work on our legacy recovery.  

You can find more info about why it exists and how to create your own zip here: [https://github.com/samsungexynos7420/MindTheGapps_Legacy](https://github.com/samsungexynos7420/MindTheGapps_Legacy)

# Downloads
{% for iden in gapps.version %}
- Android {{ iden.iden }} ([ARM64]({{ iden.arm64 }})) ([ARM]({{ iden.arm }}))
{% endfor %}

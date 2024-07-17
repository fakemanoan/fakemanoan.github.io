---
layout: default
title: "Downloads for MindTheGapps Legacy"
---
[ <-- Back](../../)

{% assign gapps = site.data.mindthegapps %}

# About MindTheGapps Legacy
MindTheGapps is created by some Lineage devs to ensure that it works correctly on custom ROMs. However, they only validate it to work on their recovery.

MindTheGapps Legacy is a modified version of MindTheGapps which will work on older TWRP versions properly.

It is a simple modification, and you can even do it yourself easily if you don't trust me. You can find more info about why it exists and how to create your own zip here: [https://github.com/samsungexynos7420/MindTheGapps_Legacy](https://github.com/samsungexynos7420/MindTheGapps_Legacy)

# Downloads
{% for iden in gapps.version %}
- Android {{ iden.iden }} ([ARM64]({{ iden.arm64 }})) ([ARM]({{ iden.arm }}))
{% endfor %}

---
layout: base
title:  'Dependencies'
generated: 'true'
permalink: zh/dep/all.html
udver: '2'
---

# Dependencies

The following table lists the 52 syntactic relations used in UD v2 for Mandarin Chinese, [36 of which are standard UD relations](http://universaldependencies.org/u/dep/) and 16 of which are specific to Mandarin Chinese. 

{% include zh-dep-table.html %}

----------

{% assign sorted = site.zh-dep | sort: 'title' %}{% for p in sorted %}
<a id="al-zh-dep/{{ p.title }}" class="al-dest"/>
<h2><code>{{ p.title }}</code>: {{ p.shortdef }}</h2>
{% if p.content contains "<!--details-->" %}    
{{ p.content | split:"<!--details-->" | first }}
<a href="{{ p.title }}" class="al-doc">See details</a>
{% else %}
{{ p.content }}
{% endif %}
<a href="{{ site.git_edit }}/{% if p.collection %}{{ p.relative_path }}{% else %}{{ p.path }}{% endif %}" target="#">edit {{ p.title }}</a>
{% endfor %}

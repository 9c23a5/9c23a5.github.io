---
layout: default
---

# Technical skills

{% for skill in site.me.my-skills %}

* **{{ skill.name }}:** {{skill.description}}

{% endfor %}

# Experience

{% for job in site.jobs %}

## {{ job.position }} at {{ job.name }}

#### {{ job.start }} - {% if job.end %} {{ job.end }} {% else %} Present {% endif %}

{% comment %}
TODO: Make h4s greyish and not bold
{% endcomment %}

{{ job.description }}

**Responsabilities:**

{% for resp in job.responsibilities %}

* **{{ resp.name }}:** {{ resp.description }}

{% endfor %}

{% endfor %}

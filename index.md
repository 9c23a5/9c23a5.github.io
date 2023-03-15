---
layout: default
---

# Technical skills

{% for skill in site.me.my-skills %}

* **{{ skill.name }}:** {{skill.description}}

{% endfor %}

# Experience

{% for job in site.jobs %}

## {{ job.position }} at {{ job.company }}

#### {{ job.start }} - {% if job.end %} {{ job.end }} {% else %} Present {% endif %}

{{ job.description }}

**Responsabilities:**

{% for resp in job.responsibilities %}

* **{{ resp.name }}:** {{ resp.description }}

{% endfor %}

{% endfor %}


# Certifications

{% for cert in site.certs %}

## {{cert.name}}

#### Certified on {{ cert.date }}

Certified by {{ cert.certifier }}.{% if cert.cert-url %} You may verify my certification [here]({{cert.cert-url}}).{% endif %}

{% endfor %}


# Education

{% for edu in site.education %}

## {{ edu.name }} at {{ edu.school }}

#### {{ edu.start }} - {% if edu.end %} {{ edu.end }} {% else %} Present {% endif %}

**Skills:**

{% for skill in learnt %}

* **{{ skill.name }}:** {{ skill.description }}

{% endfor %}

{% endfor %}

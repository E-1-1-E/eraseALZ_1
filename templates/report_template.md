# eraseALZ Drug Discovery Report – {{ virus_type }}

{% for section, data in context.items() %}
## {{ section.replace('_', ' ').title() }} Output

{% if data is mapping %}
{% for key, value in data.items() %}
### {{ key }}
{% if value is iterable and not value is string %}
{% for item in value %}
- {{ item }}
{% endfor %}
{% else %}
{{ value }}
{% endif %}
{% endfor %}
{% else %}
{{ data }}
{% endif %}

{% endfor %}

---

## Visual Summary

Below are visual representations of the data analyzed by eraseALZ pipeline.

- **Gene Target Impact Chart:**
![Gene Target Impact Chart](./soon)

- *(Additional charts such as gRNA Design Matrix, Delivery Strategy Overview, etc., may be included here as they become available.)*

---

Generated by **eraseALZ ReportGeneratorAgent**

## Publications {#publications}

### Published papers

<ul>
{% for writing in site.writings reversed %}
{% if writing.type == "article" %}
  <li>
  {{ writing.authors }}<br>
  <em>{{ writing.title }}</em><br>
  {{ writing.journal }}. 
  {% if writing.journal_link %}
    <a href="{{ writing.journal_link }}">Journal link{% if writing.open_access %} (open access){% endif %}</a>
  {% endif %}
  <br>
  {% if writing.preprint_link %}
    Preprint: <a href="{{ writing.preprint_link }}">{{ writing.preprint_name }}</a><br>
  {% endif %}
  </li><br>
{% endif %}
{% endfor %}
</ul>

### Papers in preparation, Technical reports and Quick proofs

<ul>
{% for writing in site.writings reversed %}
{% if writing.type == "prep" %}
  <li>
  {{ writing.authors }},
  <em>{{ writing.title }}</em>,
  <a href="{{ writing.preprint_link }}">{{ writing.preprint_name }}</a><br>
  </li><br>
{% endif %}
{% endfor %}
</ul>

### Other

<ul>
{% for writing in site.writings reversed %}
{% if writing.type == "other" %}
  <li>
  {{ writing.authors }},
  <em><a href="{{ writing.link }}">{{ writing.title }}</a></em>, {{ writing.description }}<br>
  </li><br>
{% endif %}
{% endfor %}
</ul>

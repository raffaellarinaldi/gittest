---
layout: default
title: Home
---

# Elenco immobili

<table>
  <thead>
    <tr>
      {% for col in site.data.properties[0] %}
        <th>{{ col[0] }}</th>
      {% endfor %}
    </tr>
  </thead>
  <tbody>
    {% for row in site.data.properties %}
      <tr>
        {% for col in row %}
          {% if col[0] == "Url" %}
            <td><a href="{{ col[1] }}" target="_blank">Link</a></td>
          {% elsif col[0] == "Image" %}
            <td><img src="{{ col[1] }}" alt="Immagine" width="120"></td>
          {% else %}
            <td>{{ col[1] }}</td>
          {% endif %}
        {% endfor %}
      </tr>
    {% endfor %}
  </tbody>
</table>
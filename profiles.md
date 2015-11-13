---
project:
  name: Profiles
layout: page
---
<div class="container">
  <ul>
  {% for profile in site.profiles %}
    <li>
      <h3><a href="{{ profile.url }}">{{ profile.profile.firstname }} {{ profile.profile.lastname }}</a></h3>
      <p>{{ profile.profile.affiliations | join: ', ' }}</p>
    </li>
  {% endfor %}
  </ul>
</div>

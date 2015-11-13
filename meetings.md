---
project:
  name: Meetings
layout: page
---
{% assign sortedmeetings = site.meetings | reverse %}

<div class="container">
  <h2>Current Meeting</h2>
  <ul>
  {% for meeting in sortedmeetings limit:1 %}
    <li>
      <h3><a href="{{ meeting.url }}">{{ meeting.title }}</a></h3>
      <p>{{ meeting.date }} at {{meeting.location}}</p>
    </li>
  {% endfor %}
  </ul>
</div>

<div class="container">
  <h2>Meetings Past</h2>
  <ul>
  {% for meeting in sortedmeetings offset:1 %}
    <li>
      <h3><a href="{{ meeting.url }}">{{ meeting.title }}</a></h3>
      <p>{{ meeting.date }} at {{meeting.location}}</p>
    </li>
  {% endfor %}
  </ul>

</div>

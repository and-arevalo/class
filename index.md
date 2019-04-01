---
layout: home
---

<h1><b>Andrés Arévalo.</b></h1>
<b>Lecturer</b> <br/>
<i>Department of Systems and Computer Engineering.<i/> <br/>
<i>Universidad Nacional de Colombia.</i> <br/>
  
## Teaching

<ul>
{% for item in site.courses %}
  {% if item.layout == 'course' %}
    <li>
	  <h2><a href="{{ item.url | relative_url}}">[{{ item.year }}-{{item.semester}}] {{ item.title }}</a></h2>
      <p>{{ item.description }}</p>
	</li>
  {% endif %}
{% endfor %}
</ul>
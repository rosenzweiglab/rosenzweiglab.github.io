---
title: People
permalink: /people/
---

{% assign people_sorted = site.people | sort: 'joined' %}
{% assign role_array = "pi|postdoc|phd|masters|nonthesis|visiting|others|alumni" | split: "|" %}

{% for role in role_array %}

{% assign people_in_role = people_sorted | where: 'position', role %}

<!-- Skip section if there's nobody -->
{% if people_in_role.size == 0 %}
  {% continue %}
{% endif %}

<div class="container">
{% if role == 'postdoc' %}
<h3>Postdoctoral Fellows</h3>
 {% elsif role == 'pi' %}
<h3>Principal Investigator</h3>
 {% elsif role == 'phd' %}
<h3>PhD Students</h3>
 {% elsif role == 'masters' %}
<h3>Masters Students</h3>
{% elsif role == 'nonthesis' %}
<h3>Non-thesis Masters Students</h3>
 {% elsif role == 'visiting' %}
<h3>Visiting Scholars</h3>
 {% elsif role == 'others' %}
<h3>Honorary Members</h3>
 {% elsif role == 'alumni' %}
<h3>Alumni</h3>
{% endif %}
</div>
{% if role != 'alumni' %}
<div class="content list people">
  {% for profile in people_sorted %}
    {% if profile.position contains role %}
      <div class="list-item-people">
        <p class="list-post-title">
          {% if profile.avatar %}
            <a href="{{ site.baseurl }}{{ profile.url }}"><img class="profile-thumbnail" src="{{ site.baseurl }}/images/people/{{ profile.avatar }}"></a>
          {% else %}
            <a href="{{ site.baseurl }}{{ profile.url }}"><img class="profile-thumbnail" src="http://evansheline.com/wp-content/uploads/2011/02/facebook-Storm-Trooper.jpg"></a>
          {% endif %}
          <a class="name" href="{{ site.baseurl }}{{ profile.url }}">{{ profile.name }}</a>
        </p>
      </div>    
    {% endif %}
  {% endfor %}
</div>
<hr>

{% else %}

| Name | Position | Current position |
| :------------- |:-------------| :-----------|
| [Elie Akoury] | Postdoc (2017 - 2020) | - |
| Vedasamitha Ramavarapu | Non-thesis Masters (2019 - 2020) | - |
| Antone Nour | Graduate Student (2012 - 2019) | - |
| Sofia Garcia-Luna | Visiting Scholar (2018) | - |




{% endif %}
{% endfor %}

<br>
<br>
<br>

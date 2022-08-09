---
layout: page
title: Staff
description: Course Staff
nav_order: 3
---

## Instructors

{% assign instructors = site.staffers | where: 'role', 'Teacher' %}
{% for staffer in instructors %}
{{ staffer }}
{% endfor %}

{% assign teaching_assistants = site.staffers | where: 'role', 'Class Monitor' %}
{% assign num_teaching_assistants = teaching_assistants | size %}
{% if num_teaching_assistants != 0 %}

## Teaching Assistants

{% for staffer in teaching_assistants %}
{{ staffer }}
{% endfor %}
{% endif %}

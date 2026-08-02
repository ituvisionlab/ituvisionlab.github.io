---
layout: page
permalink: /people/
title: People
description: 
nav: true
nav_order: 2
---
<article>
<!-- <header class="post-header">
    <h1 class="post-title">Adaptive Intelligence Lab </h1>
</header> -->

{% if site.data.team.leaders %}
    <br><h2 id="principal-investigator">Principal Investigator</h2>
    <div class="row">
        <div class="projects column">
            {% assign sorted= site.data.team.leaders | sort: "order" %}
            {% for member in sorted %}
                {% include team/leader.html member=member %}
            {% endfor %}
        </div>
    </div>
{% endif %}


{% if site.data.team.graduate_researchers %}
    <br><h2 id="graduate-researchers">Graduate Researchers</h2>
    <div class="row">
        {% assign sorted = site.data.team.graduate_researchers | sort: "order" %}
        {% for member in sorted %}
            <div class="col-sm-3 d-flex align-items-stretch">
                {% include team/active_member.html member=member %}
            </div>
        {% endfor %}
    </div>
{% endif %}


{% if site.data.team.collaborating_researchers %}
    <br><h2 id="collaborating-researchers">Collaborating Researchers</h2>
    <div class="row">
        {% assign sorted = site.data.team.collaborating_researchers | sort: "order" %}
        {% for member in sorted %}
            <div class="col-sm-3 d-flex align-items-stretch">
                {% include team/active_member.html member=member %}
            </div>
        {% endfor %}
    </div>
{% endif %}


{% if site.data.team.bachelor %}
    <br><h2 id="undergraduate-research-students">Undergraduate Research Students</h2>
    <div class="row">
        {% assign sorted= site.data.team.bachelor | sort: "order" %}
        {% for member in sorted %}
            <div class="col-sm-3 d-flex align-items-stretch">
                {% include team/active_member.html member=member %}
            </div>
        {% endfor %}
    </div>
{% endif %}

{% if site.data.team.notablealumni %}
    <br><h2 id="notable-alumni">Notable Alumni</h2>
    <div class="row">
        {% assign sorted= site.data.team.notablealumni | sort: "order" %}
        {% for member in sorted %}
            <div class="col-sm-3 d-flex align-items-stretch">
                {% include team/active_member.html member=member %}
            </div>
        {% endfor %}
    </div>
{% endif %}


</article>

---
layout: page
permalink: /people/
title: People
description: 
nav: true
# nav_order: 3
---
<article>
<!-- <header class="post-header">
    <h1 class="post-title">Adaptive Intelligence Lab </h1>
</header> -->

{% if site.data.team.leaders %}
    <br><h2 id="principal-investigator">Principal Investigator</h2>
    <div class="row">
        <div class="projects column">
            {% assign sorted= site.data.team.leaders | sort: "name" %}
            {% for member in sorted %}
                {% include team/leader.html member=member %}
            {% endfor %}
        </div>
    </div>
{% endif %}


{% if site.data.team.researchers %}
    <br><h2 id="research-fellows">Research Fellows</h2>
    <div class="row">
        {% assign sorted= site.data.team.researchers | sort: "name" %}
        {% for member in sorted %}
            <div class="col-sm-3 d-flex align-items-stretch">
                {% include team/active_member.html member=member %}
            </div>
        {% endfor %}
    </div>
{% endif %}


{% if site.data.team.mscs %}
    <br><h2 id="msc-students">MSc Students</h2>
    <div class="row">
        {% assign sorted= site.data.team.mscs | sort: "name" %}
        {% for member in sorted %}
            <div class="col-sm-3 d-flex align-items-stretch">
                {% include team/active_member.html member=member %}
            </div>
        {% endfor %}
    </div>
{% endif %}

{% if site.data.team.bscs %}
    <br><h2 id="bsc-students">BSc Students</h2>
    <div class="row">
        {% assign sorted= site.data.team.bscs | sort: "name" %}
        {% for member in sorted %}
            <div class="col-sm-3 d-flex align-items-stretch">
                {% include team/active_member.html member=member %}
            </div>
        {% endfor %}
    </div>
{% endif %}


{% if site.data.team.alumnis %}
    <br><h2 id="alumni">Alumni</h2>
    <div class="projects column">
        {% assign sorted= site.data.team.alumnis %}
        {% include team/alumni.html alumnis=sorted %}
    </div>
{% endif %}


</article>

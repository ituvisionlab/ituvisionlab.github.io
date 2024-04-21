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


{% if site.data.team.team %}
    <br><h2 id="grad-students">Graduate Students</h2>
    <div class="row">
        {% assign sorted= site.data.team.team | sort: "order" %}
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

{% if site.data.team.bachelor %}
    <br><h2 id="bsc-students">BSc Students</h2>
    <div class="row">
        {% assign sorted= site.data.team.bachelor | sort: "order" %}
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

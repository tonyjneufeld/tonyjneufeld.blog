---
layout: default
title: Score
---

<link rel="stylesheet" href="/assets/css/jim-collins.css">

<h1>My Jim Collins Daily Score</h1>

<p>This page tracks my daily self-assessment inspired by Jim Collins: quality of day, creative hours, and brief reflections.</p>

<div class="score-graph">
  {% assign logs = site.data.jim_collins_log | sort: 'date' %}
  {% for log in logs %}
    <div class="score-entry score-{{ log.score }}">
      <div class="date">{{ log.date }}</div>
      <div class="bar" style="height: {{ log.score | times: 20 | abs }}px;"></div>
      <div class="score">{{ log.score }}</div>
      <div class="hours">{{ log.creative_hours }} hrs</div>
      <div class="note">{{ log.note }}</div>
    </div>
  {% endfor %}
</div>

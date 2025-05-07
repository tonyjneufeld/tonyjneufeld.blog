---
layout: default
title: Score
---

<link rel="stylesheet" href="/assets/css/jim-collins.css">
<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>

<h1>My Daily Score</h1>

<p>This page tracks my daily self-assessment inspired by Jim Collins: quality of day, creative hours, and brief reflections. The one tweak I made is to label creative hours as Deep hours. The current thinking is that I want to better understand how I am trending towards my Deep Life goals.</p>

<canvas id="scoreChart"></canvas>

<style>
#scoreChart {
  max-height: 50px;  /* Adjust size here */
  width: 100%;
}
</style>

<div class="score-log">
  {% assign logs = site.data.jim_collins_log | sort: 'date' | reverse %}
  {% for log in logs %}
    <div class="score-entry">
      <strong>{{ log.date }}</strong>  
       - Daily Score: {{ log.score }} -  
      - Deep: {{ log.creative_hours }} hrs -  
      <em>{{ log.note }}</em>
    </div>
  {% endfor %}
</div>

<script>
// Pull data from Jekyll data file into JavaScript arrays
const labels = [{% for log in site.data.jim_collins_log | sort: 'date' %}'{{ log.date }}',{% endfor %}];
const scores = [{% for log in site.data.jim_collins_log | sort: 'date' %}{{ log.score }},{% endfor %}];
const hours = [{% for log in site.data.jim_collins_log | sort: 'date' %}{{ log.creative_hours }},{% endfor %}];

const ctx = document.getElementById('scoreChart').getContext('2d');
const scoreChart = new Chart(ctx, {
    type: 'line',
    data: {
        labels: labels,
        datasets: [
          {
            label: 'Daily Score',
            data: scores,
            yAxisID: 'yScore',
            fill: false,
            borderColor: '#2ecc71',
            backgroundColor: '#2ecc71',
            tension: 0.3,
            pointRadius: 4,
            pointBackgroundColor: function(context) {
                const val = context.raw;
                if (val === 2) return '#27ae60';
                if (val === 1) return '#2ecc71';
                if (val === 0) return '#bdc3c7';
                if (val === -1) return '#e67e22';
                if (val === -2) return '#e74c3c';
                return '#000';
            },
          },
          {
            label: 'Deep Hours',
            data: hours,
            yAxisID: 'yHours',
            fill: false,
            borderColor: '#3498db',
            backgroundColor: '#3498db',
            borderDash: [5, 5],
            tension: 0.3,
            pointRadius: 3,
          }
        ]
    },
    options: {
        scales: {
            yScore: {
                type: 'linear',
                position: 'left',
                min: -2,
                max: 2,
                ticks: { stepSize: 1 },
                title: {
                    display: true,
                    text: 'Score'
                }
            },
            yHours: {
                type: 'linear',
                position: 'right',
                title: {
                    display: true,
                    text: 'Deep Hours'
                },
                grid: {
                    drawOnChartArea: false
                }
            },
            x: {
                ticks: {
                    maxRotation: 45,
                    minRotation: 45
                }
            }
        },
        plugins: {
            legend: {
                display: true
            },
            tooltip: {
                mode: 'index',
                intersect: false
            }
        }
    }
});
</script>

---
layout: page
title: "About"
permalink: /about/
description: “Helping Canadians design a life of freedom, purpose, and financial confidence — with simple strategies for lifestyle design and long-term wealth.”
---
Hi there! 

My name is Tony Neufeld. My journey started like many Canadians. Student loans, big dreams, and the question of whether I could build for my future in Canada while still enjoying my 20s. In 2016, I found out about FIRE after I stumbled upon a [video by Mr Money Mustache](https://www.youtube.com/watch?v=8-Li_sFNc4Q). After watching that video and reading his blog, I was hooked!

What I have learned along the way is that Financial independence isn't just about money — it's about creating freedom to live your ideal lifestyle. It's about building systems and habits that grow your net worth while still enjoying your life now. A life well-lived requires intention. This means designing your career and lifestyle around what truly matters to you.

Overall, this blog's goal is to help young professionals, immigrants, indigenous folks, new parents, and families simplify their finances, build wealth, and align their money with the life they want to live—all with a distinctly Canadian lens.

This blog officially started in April 2025, and we will see how things go!

---

### Who Am I?
OK, enough about why I am starting this blog. Who am I, and what’s my story so far?
- I’m 29 years old.
- I was born in BC but have pretty much lived my whole life in Saskatchewan.
- I started my career in Sales after completing a degree in Mechanical Engineering.
- I worked in Sales and Sales Compensation for 5 years.
- I transitioned into working in Operations with a fully remote tech company for the last three years
- I got married in 2023, and we will have our first child in 2025.


---

### How am I doing?

This section is inspired by Jim Collins' daily tracking system and is designed to help me reflect on and measure progress toward a **Deep Life** — a life centered around meaning, focus, and intentionality.

The goal of this daily self-assessment is to gain clarity on:

- **Quality of the Day** – Did I live with focus, intention, and integrity?
- **Deep Hours** – How much time did I spend in undistracted, meaningful work (i.e., "Deep Work") that aligns with my personal or professional goals?
- **Brief Reflections** – A short note capturing insights, events, or patterns that affected my day.

Each day is rated on a scale from **-2 to +2** to reflect the overall **quality** of the day:

| Score | Description |
|-------|-------------|
| **+2** | Exceptional day; lived fully in line with values, high energy and presence, significant progress on goals. |
| **+1** | Good day; mostly aligned with values and goals, some meaningful progress. |
| **0**  | Neutral day; mixed focus, little progress, or went through the motions. |
| **-1** | Below average; felt misaligned, distracted, or reactive. |
| **-2** | Poor day; off-track, low energy or intentionality, far from the Deep Life. |

Tracking this helps me see patterns over time and adjust behaviours or priorities accordingly. I plan on reviewing this monthly as time goes on.

<div class="score-log">
  {% assign logs = site.data.jim_collins_log | sort: 'date' %}
  {% for log in logs %}
  {% endfor %}
</div>

<link rel="stylesheet" href="/assets/css/jim-collins.css">
<script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
<canvas id="scoreChart"></canvas>

<style>
#scoreChart {
  max-height: 400px;  /* Adjust size here */
  width: 100%;
}
</style>

<script>
// Pull data from Jekyll data file into JavaScript arrays (sorted oldest to newest)
const labels = [{% for log in logs %}'{{ log.date }}',{% endfor %}];
const scores = [{% for log in logs %}{{ log.score }},{% endfor %}];
const hours = [{% for log in logs %}{{ log.creative_hours }},{% endfor %}];

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
            borderColor: '#3b3d3c',
            backgroundColor: '#3b3d3c',
            tension: 0.3,
            pointRadius: 4,
            pointBackgroundColor: function(context) {
                const val = context.raw;
                if (val === 2) return '#2ecc71';
                if (val === 1) return '#3498db';
                if (val === 0) return '#000000';
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
            borderColor: '#38250E',
            backgroundColor: '#38250E',
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
                },
                title: {
                    display: true,
                    text: 'Date'
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


---

### I have some long-term ambitions…
- ~~Graduate from Engineering~~ (2017)
- ~~Find a fully-remote job~~ (2022)
- ~~Get married~~ (2023)
- Reach CoastFIRE
- Get 100 subscribers in a year on the blog
- Be a super dad
- Reach Financial Independence

---

### Stay in touch
Click the button in the bottom corner if you want to grab a virtual or in-person coffee!

---

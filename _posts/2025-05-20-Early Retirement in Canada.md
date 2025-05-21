---  
layout: post  
title:  "The Shockingly Simple Math Behind Early Retirement... and Why It's Less Risky in Canada."  
---

Nearly thirteen years ago, Mr. Money Mustache wrote his iconic blog post, ["The Shockingly Simple Math Behind Early Retirement](https://www.mrmoneymustache.com/2012/01/13/the-shockingly-simple-math-behind-early-retirement/)." This post changed how I think about my career and is still relevant today. Although this article is written from an American perspective, I would argue that this equation is even simpler in Canada. 

In its simplest form, your time to retire depends only on one factor:

---
> "Your household savings rate, as a percentage of your take-home pay"  
> "Your savings rate is determined by **how much you** **take home each year** and **how much you can live on**."
---

Simple right? 

To put it in perspective, Statistics Canada reported that the average savings rate in Canada as of Q4 2024 was 6.1%. Below is a conservative estimate of how long it will take to retire based on incrementally increasing savings rates:

| Savings Rate | Years to Retirement |  
|--------------|---------------------|  
| 5%           | 73                  |  
| **6.1%**         | **69**                  |  
| 10%          | 57                  |  
| 15%          | 47                  |  
| 20%          | 40                  |  
| 25%          | 35                  |  
| 30%          | 30                  |  
| 35%          | 26                  |  
| 40%          | 23                  |  
| 45%          | 20                  |  
| 50%          | 17                  |  
| 55%          | 15                  |  
| 60%          | 13                  |  
| 65%          | 11                  |  
| 70%          | 9                   |  
| 75%          | 7                   |  
| 80%          | 5                   |  
| 85%          | 4                   |  
| 90%          | 2                   |  
| 95%          | 1                   |

As you can see, the average Canadian in 2025 is not saving enough for retirement. However, there is an asterisk here because if you live and work in Canada for your career, you can qualify for **Old Age Security (OAS)** and the **Canada Pension Plan (CPP**). 

When I consider my situation, I do not want to work or earn money until I am 65\. I also don’t want to make significant lifestyle changes at that time. Most importantly, I want to be in control of my retirement; I do not want to have to rely on CPP and OAS being around to do it.

While many fear early retirement due to health insurance costs or market volatility, Canada’s social systems reduce the risk. Below are a couple of examples of why retiring early in Canada can be less risky.

## Universal Healthcare

No need for private insurance or job-linked coverage. Doctor visits, emergency care, and surgeries are 100% covered. In the US, private health insurance costs vary widely, but on average, an individual pays about $7,739 annually, and a family pays around $22,221.

## Public Pensions (CPP & OAS)

As mentioned, we have CPP and OAS in Canada, which have a couple of catches.

For CPP, you can earn up to **$1,433 monthly** at 65 (before taxes, 2025 maximum). To receive the maximum CPP retirement pension at age 65, you must have made maximum contributions for at least 39 years. The actual amount you receive depends on your earnings and contributions during your working years. 

To qualify for the full OAS amount, you must have resided in Canada for at least 40 years after turning 18\. If you have lived in Canada for fewer years, your OAS pension will be prorated accordingly.  The maximum OAS payment at 65 is **$728 monthly** (before taxes, 2025 maximum).

If you have always paid the maximum into CPP and OAS, your maximum annual earnings will be ***$25,932 ($2,161 per month) in 2025***.

## Family Support if You’re a Young Parent

Canada Child Benefit (CCB) is incredibly generous and tax-free—your lower early retirement income \= higher CCB.  The maximum annual amount per child is **$7,437 per year** if they are under 6 years old, and it applies if your family's net income is under \~$34,863, and gradually reduces above that. These amounts are **not taxed** **or counted as income** for calculating other benefits. Just need to be a resident of Canada and file taxes annually.



As much as I love all of the math behind early retirement, I believe there are steps that you must take as you embark on this journey to ensure that when you get there (and you will get there), you are left with a [fulfilling life that you love](https://tonyneufeld.blog/2025/04/28/Boulders/).

With that all being said, feel free to take a look at where you land with this very simple and conservative early retirement calculator:

---

<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Years to Retirement Calculator</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    .container {
      width: 100%;
      max-width: 600px;
      display: flex;
      flex-direction: column;
      gap: 2rem;
    }
    .calculator {
      display: flex;
      flex-direction: column;
      gap: 1rem;
      padding: 2rem;
      background: var(--card-bg);
      border-radius: 8px;
      box-shadow: 0 0 20px rgba(255 255 255 / 0.05);
    }
    .calculator input {
      padding: 0.6rem;
      font-size: 1rem;
      border: 1px solid var(--input-border);
      border-radius: 5px;
      background: var(--input-bg);
      color: var(--text-color);
    }
    .calculator input::placeholder {
      color: #999;
    }
    .result {
      font-size: 1.2rem;
      font-weight: bold;
      text-align: center;
    }
    details {
      font-size: 0.95rem;
      background: var(--card-bg);
      border-radius: 8px;
      padding: 1rem 1.2rem;
      box-shadow: 0 0 20px rgba(255 255 255 / 0.05);
      color: #eee;
      transition: background 0.3s ease;
    }
    details[open] {
      background: var(--card-bg);
    }
    summary {
      font-weight: 600;
      cursor: pointer;
      outline: none;
      list-style: none;
      user-select: none;
      position: relative;
      padding-right: 1.5rem;
    }
    summary::marker {
      display: none;
    }
    summary::after {
      content: "▸";
      position: absolute;
      right: 0;
      top: 50%;
      transform: translateY(-50%);
      transition: transform 0.3s ease;
      color: #ccc;
    }
    details[open] summary::after {
      transform: translateY(-50%) rotate(90deg);
      color: #fff;
    }
    details > *:not(summary) {
      opacity: 0;
      max-height: 0;
      overflow: hidden;
      transition: opacity 0.3s ease, max-height 0.3s ease;
    }
    details[open] > *:not(summary) {
      opacity: 1;
      max-height: 1000px;
    }
    ul {
      margin-top: 1rem;
      padding-left: 1.2rem;
      line-height: 1.6;
      color: #ddd;
    }
    ul li {
      margin-bottom: 0.5rem;
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="calculator">
      <input type="number" id="age" placeholder="Current Age" min="0" step="1" />
      <input type="text" id="income" placeholder="Annual Household Income (after-tax)" />
      <input type="text" id="spending" placeholder="Annual Household Spending" />
      <input type="text" id="networth" placeholder="Current Invested Assets" />
      <div class="result" id="savingsRate">Savings Rate: —</div>
      <div class="result" id="yearsToRetire">Years to Retirement: —</div>
      <div class="result" id="retirementAge">Estimated Retirement Age: —</div>
    </div>
    <details>
      <summary>Assumptions</summary>
      <ul>
        <li>All values are after tax (income, spending, returns).</li>
        <li>Annual expenses remain constant through retirement.</li>
        <li>You will not draw down your principal — you live off investment returns.</li>
        <li>Investment returns are inflation-adjusted (4% real return).</li>
        <li>No windfalls, inheritances, or major lifestyle changes are included.</li>
        <li>You maintain consistent income and savings until retirement.</li>
        <li>Retirement means financial independence, not necessarily stopping work.</li>
      </ul>
    </details>
  </div>

  <script>
    const ageInput = document.getElementById('age');
    const incomeInput = document.getElementById('income');
    const spendingInput = document.getElementById('spending');
    const networthInput = document.getElementById('networth');
    const savingsRateEl = document.getElementById('savingsRate');
    const yearsToRetireEl = document.getElementById('yearsToRetire');
    const retirementAgeEl = document.getElementById('retirementAge');
    const r = 0.04;

    function formatNumber(value) {
      return value.toLocaleString('en-US');
    }

    function parseNumber(value) {
      return parseFloat(value.replace(/,/g, ''));
    }

    function formatInput(e) {
      const input = e.target;
      const value = input.value.replace(/,/g, '');
      if (!isNaN(value) && value !== '') {
        input.value = formatNumber(Number(value));
      }
      calculate();
    }

    function calculate() {
      const age = parseInt(ageInput.value, 10);
      const income = parseNumber(incomeInput.value);
      const spending = parseNumber(spendingInput.value);
      const networth = parseNumber(networthInput.value);

      if (isFinite(age) && isFinite(income) && isFinite(spending) && isFinite(networth) &&
          income > 0 && spending >= 0 && networth >= 0 && income > spending && age >= 0) {

        const savingsRate = (income - spending) / income;
        savingsRateEl.textContent = `Savings Rate: ${(savingsRate * 100).toFixed(1)}%`;

        const numerator = Math.log(income / ((networth * r) + income - spending));
        const denominator = Math.log(1 + r);
        const years = numerator / denominator;

        if (isFinite(years) && years >= 0) {
          const roundedYears = Math.round(years);
          const estimatedAge = age + roundedYears;
          yearsToRetireEl.textContent = `Years to Retirement: ${roundedYears}`;
          retirementAgeEl.textContent = `Estimated Retirement Age: ${estimatedAge}`;
        } else {
          yearsToRetireEl.textContent = `Years to Retirement: ∞`;
          retirementAgeEl.textContent = `Estimated Retirement Age: ∞`;
        }

      } else {
        savingsRateEl.textContent = `Savings Rate: —`;
        yearsToRetireEl.textContent = `Years to Retirement: —`;
        retirementAgeEl.textContent = `Estimated Retirement Age: —`;
      }
    }

    [ageInput, incomeInput, spendingInput, networthInput].forEach(input => {
      input.addEventListener('input', input === ageInput ? calculate : formatInput);
    });
  </script>
</body>
</html>

---



---
layout: post
title: "How Much Do I Need to Retire in Saskatchewan?"
date: 2026-03-28 09:00:00 -0600
categories: [Personal Finance, Retirement]
tags: [saskatchewan, retirement, fire, 4% rule, calculator]
description: "A simple calculator to find your Saskatchewan retirement number. Track your spending for one month, plug it in, and find out how much you actually need."
---

*You don't need a financial advisor to answer this question. You need a pen, a month of patience, and about five minutes with the calculator below.*

Most people I talk to have no idea how much they need to retire. They've heard numbers thrown around — a million dollars, two million, "as much as possible" — and the vagueness keeps them frozen. The truth is, your retirement number is personal. It's based on one thing: **how much you actually spend.**

Not how much you earn. Not how much your neighbour has saved. How much you spend.

And if you live in Saskatchewan, that number is probably lower than you think.

---

## The 4% Rule — Your Retirement Number in One Equation

The 4% rule comes from the [Trinity Study](https://en.wikipedia.org/wiki/Trinity_study), which found that if you withdraw 4% of your investment portfolio each year, your money has historically lasted 30+ years — even through recessions, crashes, and inflation.

The math is dead simple:

**Annual Spending x 25 = Your Retirement Number**

That's it. If you spend $40,000 a year, you need $1,000,000 invested. If you spend $30,000, you need $750,000. Spend $50,000? You need $1,250,000.

The multiplier of 25 is just the inverse of 4% (1 ÷ 0.04 = 25). You're building a portfolio large enough that you can live off the returns without touching the principal.

### Why This Works Especially Well in Saskatchewan

Saskatchewan has a lower cost of living than most of Canada. Housing in Saskatoon and Regina is a fraction of what you'd pay in Vancouver or Toronto. Groceries are PST-exempt. Heating costs are real, but predictable with budget billing. A comfortable life here costs less, which means your retirement number is smaller.

On top of that, if you've worked in Canada, you'll likely receive **CPP** (up to $1,433/month at 65) and **OAS** (up to $728/month at 65). That's up to $25,932 per year in government income that *reduces* how much your portfolio needs to cover.

---

## Step 1: Track Your Spending for One Month

Before you touch the calculator, I need you to do one thing: **track every dollar you spend for one month.**

Don't change your habits. Don't try to be "good." Just observe. Use a spreadsheet, a notes app, or a piece of paper on the fridge. Every coffee, every grocery run, every bill, every subscription.

Here's what to capture:

- **Housing** — rent/mortgage, property tax, insurance, maintenance
- **Utilities** — SaskPower, SaskEnergy, water, internet, phone
- **Transportation** — car payment, SGI insurance, gas, maintenance, parking
- **Food** — groceries, dining out, coffee shops
- **Insurance** — health, dental, life (beyond what work covers)
- **Subscriptions** — streaming, gym, apps, memberships
- **Personal** — clothing, haircuts, gifts, hobbies
- **Everything else** — the random stuff that adds up

At the end of the month, add it all up. That's your monthly spending. Multiply by 12, and you have your annual spending — the only number that matters.

---

## Step 2: Plug It Into the Calculator

Take your numbers and drop them in below. The calculator will give you:

- **Your retirement number** — how much you need invested to retire
- **Your adjusted number** — factoring in CPP and OAS (if you plan to collect them)
- **Your current gap** — how far you are from your goal

<div class="calculator-container">
  <div class="calculator">
    <label for="monthly-spending">Monthly Spending ($)</label>
    <input type="text" id="monthly-spending" placeholder="e.g. 3,000" />

    <label for="current-savings">Current Invested Assets ($)</label>
    <input type="text" id="current-savings" placeholder="e.g. 50,000" />

    <label for="monthly-contribution">Monthly Savings / Contributions ($)</label>
    <input type="text" id="monthly-contribution" placeholder="e.g. 500" />

    <label for="current-age">Current Age</label>
    <input type="number" id="current-age" placeholder="e.g. 30" min="0" step="1" />

    <label for="include-cpp-oas">
      <input type="checkbox" id="include-cpp-oas" checked /> Include estimated CPP & OAS at 65
    </label>

    <div class="result" id="annual-spending-result">Annual Spending: —</div>
    <div class="result" id="fire-number-result">Retirement Number (4% Rule): —</div>
    <div class="result" id="adjusted-number-result">Adjusted for CPP & OAS: —</div>
    <div class="result" id="gap-result">Your Gap: —</div>
    <div class="result" id="years-result">Estimated Years to Retirement: —</div>
    <div class="result" id="retirement-age-result">Estimated Retirement Age: —</div>
  </div>

  <details>
    <summary>Assumptions & Notes</summary>
    <ul>
      <li>Uses the 4% safe withdrawal rate (Trinity Study).</li>
      <li>Investment returns assumed at 7% nominal / 4% real (after inflation).</li>
      <li>CPP estimate uses $1,433/month (2025 max at age 65) — your actual amount depends on contribution history.</li>
      <li>OAS estimate uses $728/month (2025 max at age 65) — requires 40 years of Canadian residency for full amount.</li>
      <li>CPP & OAS adjustment reduces your required portfolio by the annual value of those benefits, divided by 4%.</li>
      <li>Annual spending is assumed to stay constant (inflation-adjusted).</li>
      <li>No windfalls, inheritances, or major lifestyle changes included.</li>
      <li>This is a starting point, not a financial plan. For personalized guidance, <a href="/services/">book a free discovery call</a>.</li>
    </ul>
  </details>
</div>

<style>
  .calculator-container {
    width: 100%;
    max-width: 600px;
    display: flex;
    flex-direction: column;
    gap: 2rem;
    margin: 2rem 0;
  }
  .calculator {
    display: flex;
    flex-direction: column;
    gap: 0.75rem;
    padding: 2rem;
    background: var(--card-bg);
    border-radius: 8px;
    box-shadow: 0 0 20px rgba(255 255 255 / 0.05);
    color: var(--text-color);
    border: 1px solid var(--text-color);
  }
  .calculator label {
    font-weight: 600;
    font-size: 0.9rem;
    margin-bottom: -0.25rem;
  }
  .calculator label[for="include-cpp-oas"] {
    display: flex;
    align-items: center;
    gap: 0.5rem;
    font-weight: 400;
    margin-top: 0.5rem;
    cursor: pointer;
  }
  .calculator input[type="text"],
  .calculator input[type="number"] {
    padding: 0.6rem;
    font-size: 1rem;
    border: 1px solid var(--text-color);
    border-radius: 5px;
    background: var(--input-bg);
    color: var(--text-color);
  }
  .calculator input::placeholder {
    color: #999;
  }
  .calculator .result {
    font-size: 1.1rem;
    font-weight: bold;
    text-align: center;
    padding: 0.25rem 0;
  }
</style>

<script>
  (function() {
    const monthlySpendingInput = document.getElementById('monthly-spending');
    const currentSavingsInput = document.getElementById('current-savings');
    const monthlyContributionInput = document.getElementById('monthly-contribution');
    const currentAgeInput = document.getElementById('current-age');
    const includeCppOas = document.getElementById('include-cpp-oas');

    const annualSpendingEl = document.getElementById('annual-spending-result');
    const fireNumberEl = document.getElementById('fire-number-result');
    const adjustedNumberEl = document.getElementById('adjusted-number-result');
    const gapEl = document.getElementById('gap-result');
    const yearsEl = document.getElementById('years-result');
    const retirementAgeEl = document.getElementById('retirement-age-result');

    const realReturn = 0.04;
    const annualCppOas = (1433 + 728) * 12; // $25,932

    function fmt(n) {
      return n.toLocaleString('en-CA', { maximumFractionDigits: 0 });
    }

    function parse(v) {
      return parseFloat(v.replace(/[,$\s]/g, '')) || 0;
    }

    function formatInput(e) {
      const input = e.target;
      const raw = input.value.replace(/[,$\s]/g, '');
      if (!isNaN(raw) && raw !== '') {
        input.value = fmt(Number(raw));
      }
      calculate();
    }

    function calculate() {
      const monthlySpending = parse(monthlySpendingInput.value);
      const currentSavings = parse(currentSavingsInput.value);
      const monthlyContribution = parse(monthlyContributionInput.value);
      const age = parseInt(currentAgeInput.value, 10);
      const withCppOas = includeCppOas.checked;

      if (monthlySpending <= 0) {
        annualSpendingEl.textContent = 'Annual Spending: —';
        fireNumberEl.textContent = 'Retirement Number (4% Rule): —';
        adjustedNumberEl.textContent = 'Adjusted for CPP & OAS: —';
        gapEl.textContent = 'Your Gap: —';
        yearsEl.textContent = 'Estimated Years to Retirement: —';
        retirementAgeEl.textContent = 'Estimated Retirement Age: —';
        return;
      }

      const annualSpending = monthlySpending * 12;
      const fireNumber = annualSpending * 25;

      let adjustedNumber = fireNumber;
      if (withCppOas) {
        adjustedNumber = Math.max(0, fireNumber - (annualCppOas / realReturn));
      }

      const gap = Math.max(0, adjustedNumber - currentSavings);
      const annualContribution = monthlyContribution * 12;

      annualSpendingEl.textContent = 'Annual Spending: $' + fmt(annualSpending);
      fireNumberEl.textContent = 'Retirement Number (4% Rule): $' + fmt(fireNumber);
      adjustedNumberEl.textContent = 'Adjusted for CPP & OAS: $' + fmt(adjustedNumber);
      gapEl.textContent = 'Your Gap: $' + fmt(gap);

      // Calculate years to reach target with compound growth
      if (currentSavings >= adjustedNumber) {
        yearsEl.textContent = 'Estimated Years to Retirement: 0 — you\'re there!';
        retirementAgeEl.textContent = isFinite(age) && age >= 0
          ? 'Estimated Retirement Age: ' + age + ' — you\'re there!'
          : 'Estimated Retirement Age: —';
        return;
      }

      if (annualContribution <= 0 && currentSavings < adjustedNumber) {
        // Only growth from existing savings
        if (currentSavings <= 0) {
          yearsEl.textContent = 'Estimated Years to Retirement: ∞ (start saving!)';
          retirementAgeEl.textContent = 'Estimated Retirement Age: —';
          return;
        }
        const years = Math.log(adjustedNumber / currentSavings) / Math.log(1 + realReturn);
        const rounded = Math.ceil(years);
        yearsEl.textContent = 'Estimated Years to Retirement: ~' + rounded;
        retirementAgeEl.textContent = isFinite(age) && age >= 0
          ? 'Estimated Retirement Age: ~' + (age + rounded)
          : 'Estimated Retirement Age: —';
        return;
      }

      // Iterative calculation: savings grow at realReturn, plus annual contributions
      let balance = currentSavings;
      let years = 0;
      while (balance < adjustedNumber && years < 100) {
        balance = balance * (1 + realReturn) + annualContribution;
        years++;
      }

      if (years >= 100) {
        yearsEl.textContent = 'Estimated Years to Retirement: 100+ years';
        retirementAgeEl.textContent = 'Estimated Retirement Age: —';
      } else {
        yearsEl.textContent = 'Estimated Years to Retirement: ~' + years;
        retirementAgeEl.textContent = isFinite(age) && age >= 0
          ? 'Estimated Retirement Age: ~' + (age + years)
          : 'Estimated Retirement Age: —';
      }
    }

    [monthlySpendingInput, currentSavingsInput, monthlyContributionInput].forEach(function(input) {
      input.addEventListener('input', formatInput);
    });
    currentAgeInput.addEventListener('input', calculate);
    includeCppOas.addEventListener('change', calculate);
  })();
</script>

---

## What the Number Means (and What It Doesn't)

Your retirement number is a target, not a prison sentence. It's the point where your investments can cover your lifestyle without you needing a paycheque. A few things to keep in mind:

**It's based on today's spending.** If your lifestyle changes — kids move out, mortgage gets paid off, you move to a smaller place — your number drops. The reverse is also true.

**CPP and OAS are a bonus, not a guarantee.** I included the toggle because those benefits are real and significant for Canadians. But I'd rather you hit your number without them and treat government income as gravy. That's the position of strength you want to be in.

**You don't need to get there overnight.** The gap might look intimidating. That's fine. The point is knowing the number so you can work toward it intentionally instead of guessing.

---

## The One Thing I'd Ask You to Do This Week

Track your spending for the next 30 days. That's it. Don't optimize, don't cut anything, don't stress about it. Just write it down.

At the end of the month, plug your monthly number into the calculator above. You'll know your retirement number in five seconds. And from there, everything gets clearer — what to save, which accounts to use, and how long the road actually is.

Most people are closer than they think. Especially here on the Prairies.

*If you want help building a plan around your number, [book a free discovery call](/services/) and we'll figure it out together.*

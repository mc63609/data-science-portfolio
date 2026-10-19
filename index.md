---
title: Chen Junyang — Data Science Portfolio
---

<div class="wrap">

  <header class="hero">
    <p class="eyebrow">Data Science Portfolio</p>
    <h1>Chen Junyang</h1>
    <p class="lede">
      Data science student at the University of Macau. I turn messy public datasets into
      clear, defensible answers — and I care as much about <em>why</em> a number is true
      as about the number itself.
    </p>
    <ul class="chips">
      <li>Python</li>
      <li>pandas · NumPy</li>
      <li>Matplotlib · seaborn</li>
      <li>Jupyter</li>
      <li>Exploratory data analysis</li>
      <li>Data visualisation</li>
      <li>Git · GitHub Pages</li>
    </ul>
  </header>

  <section class="about">
    <h2>About</h2>
    <p>
      I work mostly in Python: cleaning a dataset until it can be trusted, then testing a
      question against it instead of assuming the answer. My current focus is exploratory
      analysis and visual storytelling — building charts that make a finding obvious in one
      glance, and writing down the caveats that a single summary statistic would hide.
    </p>
    <p>
      This page is my portfolio: each entry below links to a public repository with the
      data, the code and a README detailed enough that someone else can reproduce the
      results from a clean machine.
    </p>
  </section>

  <section class="project">
    <div class="project-head">
      <div>
        <p class="eyebrow">Project 01</p>
        <h2>Does body size predict Olympic success?</h2>
        <p class="meta">Rio 2016 · 11,538 athletes · 28 sports · Python, pandas, Matplotlib</p>
      </div>
      <span class="status status-done">Completed</span>
    </div>

    <div class="question">
      <p class="label">Research question</p>
      <p>
        Were Rio 2016 medalists systematically taller and heavier than athletes who did not
        medal — and is that advantage the same in every sport?
      </p>
    </div>

    <figure>
      <img src="images/fig1_medal_rate_by_height_quartile.png"
           alt="Bar chart of medal rate by height quartile, split by sex" />
      <figcaption>
        Medal rate by height quartile, computed within each sex. Rio 2016, 11,208 athletes
        with a recorded height.
      </figcaption>
    </figure>

    <p class="label">What the data shows</p>
    <ul class="findings">
      <li>
        <strong>Size helps on average.</strong> The tallest quartile of athletes medals
        <strong>1.6×</strong> as often as the shortest among men (22.3% vs 13.7%) and
        <strong>1.9×</strong> as often among women (23.7% vs 12.3%).
      </li>
      <li>
        <strong>But the advantage is sport-specific.</strong> Standardised height differences
        between medalists and non-medalists range from <strong>−0.43</strong> in table tennis
        to <strong>+0.51</strong> in volleyball and taekwondo — the same body type that wins
        one sport loses another.
      </li>
      <li>
        <strong>Where mass is regulated, height stops mattering.</strong> Weightlifting
        (−0.10) and wrestling (+0.05) sit near zero: inside a weight class, extra height buys
        nothing.
      </li>
    </ul>

    <div class="figure-grid">
      <figure>
        <img src="images/fig2_sport_height_effects.png"
             alt="Diverging bar chart of standardised height differences by sport" />
        <figcaption>
          Height difference between medalists and non-medalists, per sport (Cohen's d on
          within-sex z-scores).
        </figcaption>
      </figure>
      <figure>
        <img src="images/fig3_body_size_map.png"
             alt="Scatter plot of median height against median weight by sport and sex" />
        <figcaption>
          The Olympic body map: median height vs. median weight per sport and sex, bubble area
          proportional to athlete count.
        </figcaption>
      </figure>
    </div>

    <div class="takeaway">
      <p class="label">Takeaway &amp; one limitation</p>
      <p>
        "Taller athletes win more" is true only as an average. Split by sport, body size is an
        advantage in volleyball and cycling, irrelevant in shooting and archery, and a
        disadvantage in gymnastics and table tennis. The biggest caveat is that every member
        of a medalling squad is counted individually, so team sports show inflated medal
        rates (25% in basketball vs 7.4% in athletics) — part of that effect is squad
        selection, not individual performance.
      </p>
    </div>

    <div class="actions">
      <a class="btn" href="https://github.com/mc63609/data-science-project">View the repository</a>
      <a class="btn btn-ghost" href="https://github.com/mc63609/data-science-project/blob/main/notebooks/rio2016_body_size_analysis.ipynb">Open the notebook</a>
    </div>
  </section>

  <section class="next">
    <h2>What I would do next</h2>
    <p>
      The current analysis stops at sport level. The next iteration would use event-level data
      (100 m vs. shot put), fit a logistic regression of medalling on height, weight, age and
      sport fixed effects, and re-run everything on individual sports only as a robustness
      check on the team-sport inflation.
    </p>
  </section>

  <footer>
    <p>Chen Junyang · CISC7204 Data Science Portfolio · University of Macau</p>
    <p><a href="https://github.com/mc63609">github.com/mc63609</a></p>
  </footer>

</div>

<style>
  .wrap {
    --ink: #1f2933;
    --muted: #6b7684;
    --line: #e4e7eb;
    --accent: #2f6f9f;
    --gold: #c8a04a;
    max-width: 860px;
    margin: 0 auto;
    padding: 56px 24px 64px;
    color: var(--ink);
    font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", "Helvetica Neue", Arial,
      "PingFang SC", "Microsoft YaHei", sans-serif;
    font-size: 17px;
    line-height: 1.7;
    -webkit-font-smoothing: antialiased;
  }
  .wrap h1, .wrap h2, .wrap p, .wrap ul, .wrap figure { margin: 0; }
  .wrap h1 {
    font-size: 44px;
    line-height: 1.15;
    letter-spacing: -0.02em;
    font-weight: 700;
    margin: 6px 0 14px;
  }
  .wrap h2 {
    font-size: 25px;
    line-height: 1.3;
    letter-spacing: -0.01em;
    font-weight: 650;
    margin: 0 0 12px;
  }
  .wrap a { color: var(--accent); text-decoration: none; border-bottom: 1px solid rgba(47,111,159,.28); }
  .wrap a:hover { border-bottom-color: var(--accent); }
  .eyebrow {
    font-size: 12px;
    font-weight: 600;
    letter-spacing: 0.14em;
    text-transform: uppercase;
    color: var(--muted);
  }
  .lede { font-size: 19px; color: #3b4652; max-width: 44em; }
  .hero { padding-bottom: 34px; border-bottom: 1px solid var(--line); }
  .chips { list-style: none; padding: 0; display: flex; flex-wrap: wrap; gap: 8px; margin-top: 24px; }
  .chips li {
    font-size: 13.5px;
    color: #3b4652;
    background: #f4f6f8;
    border: 1px solid var(--line);
    border-radius: 999px;
    padding: 4px 12px;
  }
  .about { padding: 34px 0 6px; }
  .about p + p { margin-top: 12px; }
  .about p, .next p, .takeaway p, .question p, .findings li { color: #3b4652; }

  .project { padding: 34px 0 8px; margin-top: 22px; border-top: 1px solid var(--line); }
  .project-head { display: flex; align-items: flex-start; justify-content: space-between; gap: 18px; flex-wrap: wrap; }
  .project-head h2 { margin: 4px 0 6px; font-size: 28px; }
  .meta { font-size: 14.5px; color: var(--muted); }
  .status {
    font-size: 12.5px;
    font-weight: 600;
    letter-spacing: 0.04em;
    padding: 5px 12px;
    border-radius: 999px;
    white-space: nowrap;
  }
  .status-done { color: #1d6b4f; background: #e6f4ee; border: 1px solid #c6e5d7; }

  .question {
    margin: 22px 0 26px;
    padding: 16px 20px;
    border-left: 3px solid var(--gold);
    background: #fbf9f4;
    border-radius: 0 8px 8px 0;
  }
  .question p:last-child { font-size: 17.5px; }
  .label {
    font-size: 12px;
    font-weight: 650;
    letter-spacing: 0.12em;
    text-transform: uppercase;
    color: var(--muted);
    margin-bottom: 6px;
  }
  .wrap figure { margin: 26px 0; }
  .wrap img {
    width: 100%;
    height: auto;
    display: block;
    border: 1px solid var(--line);
    border-radius: 10px;
    background: #fff;
  }
  figcaption { font-size: 13.5px; color: var(--muted); margin-top: 9px; line-height: 1.55; }
  .figure-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 22px; margin: 26px 0; }
  .figure-grid figure { margin: 0; }

  .findings { padding-left: 0; list-style: none; margin: 10px 0 0; }
  .findings li {
    position: relative;
    padding-left: 20px;
    margin-bottom: 12px;
  }
  .findings li::before {
    content: "";
    position: absolute;
    left: 0;
    top: 11px;
    width: 7px;
    height: 7px;
    border-radius: 50%;
    background: var(--gold);
  }
  .takeaway {
    margin-top: 24px;
    padding: 18px 20px;
    background: #f7f8fa;
    border-radius: 10px;
  }
  .actions { display: flex; flex-wrap: wrap; gap: 12px; margin-top: 26px; }
  .btn {
    display: inline-block;
    font-size: 15px;
    font-weight: 600;
    padding: 10px 20px;
    border-radius: 8px;
    background: var(--accent);
    color: #fff !important;
    border: 1px solid var(--accent) !important;
    transition: background .15s ease;
  }
  .btn:hover { background: #275d85; }
  .btn-ghost {
    background: #fff;
    color: var(--accent) !important;
    border: 1px solid #cfd8e3 !important;
  }
  .btn-ghost:hover { background: #f4f7fa; }

  .next { margin-top: 34px; padding-top: 30px; border-top: 1px solid var(--line); }
  footer {
    margin-top: 40px;
    padding-top: 22px;
    border-top: 1px solid var(--line);
    font-size: 14px;
    color: var(--muted);
  }
  footer p + p { margin-top: 4px; }

  @media (max-width: 680px) {
    .wrap { padding: 36px 18px 48px; font-size: 16px; }
    .wrap h1 { font-size: 34px; }
    .wrap h2 { font-size: 22px; }
    .figure-grid { grid-template-columns: 1fr; }
  }
</style>

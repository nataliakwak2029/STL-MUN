<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta name="theme-color" content="#090909">
  <meta name="description" content="St. Laurence High School Model United Nations | STLMUN | Burbank, Illinois">
  <title>St. Laurence Model United Nations | STLMUN</title>

  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=Playfair+Display:wght@600;700;800&display=swap" rel="stylesheet">

  <style>
    :root {
      --black: #080808;
      --black-soft: #111111;
      --gold: #c7a64a;
      --gold-light: #e5ca70;
      --cream: #faf8f1;
      --cream-dark: #f0ede3;
      --white: #ffffff;
      --text: #171717;
      --muted: #68655e;
      --border: rgba(0,0,0,.12);
      --radius: 24px;
      --max: 1180px;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      background: var(--cream);
      color: var(--text);
      font-family: "DM Sans", Arial, sans-serif;
      line-height: 1.6;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    img {
      width: 100%;
      display: block;
    }

    .container {
      width: min(var(--max), calc(100% - 40px));
      margin: auto;
    }

    h1, h2, h3 {
      font-family: "Playfair Display", Georgia, serif;
      line-height: 1.08;
    }

    h2 {
      font-size: clamp(2.2rem, 5vw, 4rem);
      letter-spacing: -.035em;
    }

    .eyebrow {
      display: inline-flex;
      align-items: center;
      gap: 10px;
      color: var(--gold);
      font-size: .72rem;
      font-weight: 800;
      letter-spacing: .17em;
      text-transform: uppercase;
    }

    .eyebrow::before {
      content: "";
      width: 28px;
      height: 1px;
      background: currentColor;
    }

    .btn {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      min-height: 48px;
      padding: 0 20px;
      border-radius: 999px;
      font-size: .88rem;
      font-weight: 700;
      transition: .2s ease;
    }

    .btn-gold {
      background: var(--gold);
      color: var(--black);
    }

    .btn-gold:hover {
      background: var(--gold-light);
      transform: translateY(-2px);
    }

    .btn-dark {
      background: var(--black);
      color: white;
    }

    .btn-dark:hover {
      background: #252525;
      transform: translateY(-2px);
    }

    /* NAVIGATION */

    .nav {
      position: fixed;
      top: 0;
      left: 0;
      right: 0;
      z-index: 100;
      background: rgba(8,8,8,.92);
      backdrop-filter: blur(18px);
      border-bottom: 1px solid rgba(255,255,255,.08);
    }

    .nav-inner {
      height: 74px;
      display: flex;
      align-items: center;
      justify-content: space-between;
    }

    .brand {
      display: flex;
      align-items: center;
      gap: 12px;
      color: white;
    }

    .crest {
      width: 40px;
      height: 40px;
      border: 1px solid rgba(229,202,112,.65);
      border-radius: 50%;
      display: grid;
      place-items: center;
      color: var(--gold-light);
      font-family: Georgia, serif;
      font-size: 14px;
      position: relative;
    }

    .crest::after {
      content: "";
      position: absolute;
      inset: 5px;
      border: 1px solid rgba(229,202,112,.35);
      border-radius: 50%;
    }

    .brand small {
      display: block;
      color: #999;
      font-size: .58rem;
      letter-spacing: .14em;
      text-transform: uppercase;
    }

    .brand strong {
      display: block;
      font-size: .9rem;
      letter-spacing: .02em;
    }

    .nav-links {
      display: flex;
      gap: 25px;
      color: #d8d8d8;
      font-size: .82rem;
      font-weight: 600;
    }

    .nav-links a:hover {
      color: var(--gold-light);
    }

    .menu {
      display: none;
      background: none;
      border: none;
      color: white;
      font-size: 1.5rem;
      cursor: pointer;
    }

    /* HERO */

    .hero {
      min-height: 100vh;
      padding: 120px 0 80px;
      background: var(--black);
      color: white;
      display: flex;
      align-items: center;
      position: relative;
      overflow: hidden;
    }

    .hero::before {
      content: "";
      position: absolute;
      width: 720px;
      height: 720px;
      border-radius: 50%;
      right: -300px;
      top: -230px;
      border: 1px solid rgba(199,166,74,.18);
      box-shadow:
        0 0 0 90px rgba(199,166,74,.025),
        0 0 0 180px rgba(199,166,74,.02);
    }

    .hero-grid {
      display: grid;
      grid-template-columns: 1fr .92fr;
      gap: 70px;
      align-items: center;
      position: relative;
    }

    .hero h1 {
      font-size: clamp(3.2rem, 7vw, 6.5rem);
      letter-spacing: -.055em;
      margin: 18px 0 24px;
      max-width: 800px;
    }

    .hero h1 span {
      color: var(--gold-light);
    }

    .hero-lead {
      max-width: 650px;
      color: #c7c7c7;
      font-size: 1.05rem;
    }

    .hero-actions {
      display: flex;
      flex-wrap: wrap;
      gap: 12px;
      margin-top: 32px;
    }

    .hero-location {
      margin-top: 26px;
      color: #858585;
      font-size: .82rem;
    }

    .hero-photo {
      position: relative;
      padding: 10px;
      border: 1px solid rgba(255,255,255,.15);
      background: rgba(255,255,255,.03);
      transform: rotate(1deg);
    }

    .hero-photo img {
      aspect-ratio: 4 / 3;
      object-fit: cover;
    }

    .photo-tag {
      position: absolute;
      left: -18px;
      bottom: 25px;
      padding: 12px 17px;
      background: var(--gold);
      color: var(--black);
      font-size: .7rem;
      font-weight: 800;
      letter-spacing: .08em;
      text-transform: uppercase;
    }

    /* GENERAL SECTIONS */

    section {
      padding: 105px 0;
    }

    .section-head {
      display: grid;
      grid-template-columns: .75fr 1.25fr;
      gap: 50px;
      align-items: end;
      margin-bottom: 50px;
    }

    .section-head p {
      color: var(--muted);
      max-width: 650px;
    }

    /* ABOUT */

    .about {
      background: white;
      border-bottom: 1px solid var(--border);
    }

    .about-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 25px;
    }

    .about-card {
      padding: 36px;
      border-radius: var(--radius);
      background: #f5f1e5;
    }

    .about-card.dark {
      background: var(--black);
      color: white;
    }

    .about-card h3 {
      font-size: 1.8rem;
      margin-bottom: 15px;
    }

    .about-card p {
      opacity: .78;
    }

    /* WHAT IS MUN */

    .mun {
      background: var(--cream);
    }

    .steps {
      display: grid;
      grid-template-columns: repeat(4, 1fr);
      gap: 14px;
    }

    .step {
      min-height: 235px;
      padding: 26px;
      background: white;
      border: 1px solid var(--border);
      border-radius: 20px;
      position: relative;
      overflow: hidden;
    }

    .step::after {
      content: attr(data-number);
      position: absolute;
      right: 15px;
      bottom: -25px;
      color: rgba(199,166,74,.10);
      font: 800 8rem/1 "Playfair Display";
    }

    .step-number {
      color: var(--gold);
      font-size: .72rem;
      font-weight: 800;
      letter-spacing: .14em;
    }

    .step h3 {
      font-size: 1.35rem;
      margin: 28px 0 10px;
    }

    .step p {
      color: var(--muted);
      font-size: .88rem;
      position: relative;
      z-index: 1;
    }

    /* CONFERENCES */

    .conferences {
      background: var(--black);
      color: white;
    }

    .conferences .section-head p {
      color: #aaa;
    }

    .conference-grid {
      display: grid;
      grid-template-columns: 1.05fr .95fr;
      gap: 45px;
      align-items: start;
    }

    .conference-photo {
      position: sticky;
      top: 105px;
    }

    .conference-photo img {
      aspect-ratio: 4 / 3;
      object-fit: cover;
    }

    .caption {
      color: #888;
      font-size: .72rem;
      margin-top: 10px;
    }

    .conference-list {
      display: grid;
      gap: 14px;
    }

    .conference-card {
      padding: 25px 26px;
      border: 1px solid rgba(255,255,255,.12);
      border-radius: 20px;
      background: rgba(255,255,255,.035);
      transition: .2s ease;
    }

    .conference-card:hover {
      border-color: rgba(229,202,112,.5);
      transform: translateX(4px);
    }

    .conference-meta {
      color: var(--gold-light);
      font-size: .7rem;
      font-weight: 800;
      letter-spacing: .13em;
      text-transform: uppercase;
    }

    .conference-card h3 {
      font-size: 1.6rem;
      margin: 9px 0;
    }

    .conference-card p {
      color: #aaa;
      font-size: .9rem;
    }

    .recognition {
      margin-top: 15px;
      padding: 14px 0 14px 20px;
      border-left: 2px solid var(--gold);
    }

    .recognition strong {
      display: block;
    }

    .recognition span {
      color: #999;
      font-size: .83rem;
    }

    /* MEETINGS */

    .meetings {
      background: white;
    }

    .meeting-grid {
      display: grid;
      grid-template-columns: .9fr 1.1fr;
      gap: 65px;
    }

    .meeting-box {
      padding: 32px;
      background: #f7f4ea;
      border: 1px solid var(--border);
      border-radius: 24px;
    }

    .meeting-box h3 {
      font-size: 1.8rem;
      margin-bottom: 14px;
    }

    .meeting-box > p {
      color: var(--muted);
    }

    .meeting-list {
      display: grid;
      gap: 13px;
      margin-top: 25px;
    }

    .meeting-item {
      display: flex;
      gap: 13px;
    }

    .dot {
      flex: 0 0 8px;
      height: 8px;
      margin-top: 9px;
      border-radius: 50%;
      background: var(--gold);
    }

    .meeting-item strong {
      display: block;
      font-size: .92rem;
    }

    .meeting-item span {
      color: var(--muted);
      font-size: .83rem;
    }

    .contributions {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 14px;
    }

    .contribution-card {
      padding: 26px;
      border: 1px solid var(--border);
      border-radius: 18px;
    }

    .contribution-number {
      color: var(--gold);
      font-weight: 800;
    }

    .contribution-card h3 {
      font-size: 1.25rem;
      margin: 12px 0 7px;
    }

    .contribution-card p {
      color: var(--muted);
      font-size: .84rem;
    }

    /* TEAM */

    .team {
      background: var(--cream-dark);
    }

    .team-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 45px;
      align-items: center;
    }

    .team-photo img {
      aspect-ratio: 1.05 / 1;
      object-fit: cover;
    }

    .team-content h2 {
      margin: 16px 0;
    }

    .team-content > p {
      color: var(--muted);
    }

    .leaders {
      display: grid;
      gap: 12px;
      margin-top: 30px;
    }

    .leader {
      display: flex;
      justify-content: space-between;
      padding: 16px 0;
      border-bottom: 1px solid rgba(0,0,0,.1);
    }

    .leader strong {
      font-size: .94rem;
    }

    .leader span {
      color: var(--muted);
      font-size: .73rem;
      letter-spacing: .1em;
      text-transform: uppercase;
    }

    .impact {
      display: grid;
      grid-template-columns: repeat(3,1fr);
      gap: 12px;
      margin-top: 35px;
    }

    .impact-card {
      background: white;
      padding: 22px;
      border-radius: 18px;
    }

    .impact-card b {
      color: var(--gold);
      font: 700 2.1rem "Playfair Display";
    }

    .impact-card span {
      display: block;
      color: var(--muted);
      font-size: .76rem;
    }

    /* GALLERY */

    .gallery {
      background: white;
    }

    .gallery-grid {
      display: grid;
      grid-template-columns: 1.15fr .85fr;
      grid-template-rows: 260px 260px;
      gap: 14px;
    }

    .gallery-card {
      overflow: hidden;
      border-radius: 20px;
      position: relative;
      background: #ddd;
    }

    .gallery-card:first-child {
      grid-row: span 2;
    }

    .gallery-card img {
      height: 100%;
      object-fit: cover;
      transition: transform .5s ease;
    }

    .gallery-card:hover img {
      transform: scale(1.04);
    }

    .gallery-card::after {
      content: "";
      position: absolute;
      left: 0;
      right: 0;
      bottom: 0;
      height: 45%;
      background: linear-gradient(transparent, rgba(0,0,0,.7));
    }

    .gallery-label {
      position: absolute;
      z-index: 2;
      left: 20px;
      bottom: 18px;
      color: white;
      font-size: .73rem;
      font-weight: 800;
      letter-spacing: .1em;
      text-transform: uppercase;
    }

    /* GLOBAL */

    .global {
      background: var(--black);
      color: white;
    }

    .global .section-head p {
      color: #aaa;
    }

    .flags {
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      gap: 10px;
      margin-top: 30px;
    }

    .flag {
      padding: 10px 14px;
      border: 1px solid rgba(255,255,255,.12);
      border-radius: 999px;
      background: rgba(255,255,255,.035);
      color: #d5d5d5;
      font-size: .83rem;
    }

    .flag span {
      margin-right: 7px;
    }

    /* CONTACT */

    .contact {
      background: #f3e7bb;
    }

    .contact-grid {
      display: grid;
      grid-template-columns: 1.1fr .9fr;
      gap: 55px;
      align-items: center;
    }

    .contact h2 {
      margin: 15px 0;
    }

    .contact-copy > p {
      max-width: 620px;
      color: #59564f;
    }

    .contact-buttons {
      display: flex;
      flex-wrap: wrap;
      gap: 10px;
      margin-top: 25px;
    }

    .contact-card {
      padding: 30px;
      background: white;
      border-radius: 24px;
      box-shadow: 0 16px 50px rgba(0,0,0,.08);
    }

    .contact-label {
      color: var(--muted);
      font-size: .67rem;
      font-weight: 800;
      letter-spacing: .14em;
      text-transform: uppercase;
    }

    .contact-card a {
      display: block;
      margin: 6px 0 22px;
      font-weight: 700;
    }

    .contact-card a:hover {
      color: #8b6c17;
    }

    /* FOOTER */

    footer {
      padding: 35px 0;
      background: #050505;
      color: #999;
    }

    .footer-inner {
      display: flex;
      justify-content: space-between;
      gap: 20px;
      align-items: center;
    }

    footer strong {
      color: white;
    }

    footer p,
    .footer-links {
      font-size: .76rem;
    }

    .footer-links {
      display: flex;
      gap: 18px;
    }

    .footer-links a:hover {
      color: var(--gold);
    }

    /* MOBILE */

    @media (max-width: 900px) {

      .nav-links {
        display: none;
        position: absolute;
        top: 74px;
        left: 0;
        right: 0;
        flex-direction: column;
        gap: 0;
        background: #090909;
        border-bottom: 1px solid rgba(255,255,255,.1);
      }

      .nav-links.open {
        display: flex;
      }

      .nav-links a {
        padding: 16px 20px;
        border-bottom: 1px solid rgba(255,255,255,.06);
      }

      .menu {
        display: block;
      }

      .hero-grid,
      .section-head,
      .conference-grid,
      .meeting-grid,
      .team-grid,
      .contact-grid {
        grid-template-columns: 1fr;
      }

      .hero h1 {
        font-size: clamp(3rem, 12vw, 5.2rem);
      }

      .hero-photo {
        max-width: 720px;
        margin: auto;
      }

      .conference-photo {
        position: static;
      }

      .steps {
        grid-template-columns: 1fr 1fr;
      }

      .gallery-grid {
        grid-template-columns: 1fr 1fr;
        grid-template-rows: 300px 220px;
      }

      .gallery-card:first-child {
        grid-column: span 2;
        grid-row: span 1;
      }
    }

    @media (max-width: 600px) {

      .container {
        width: min(100% - 28px, var(--max));
      }

      section {
        padding: 78px 0;
      }

      .nav-inner {
        height: 66px;
      }

      .hero {
        padding-top: 100px;
      }

      .hero-lead {
        font-size: .96rem;
      }

      .about-grid,
      .steps,
      .contributions,
      .impact,
      .gallery-grid {
        grid-template-columns: 1fr;
      }

      .gallery-grid {
        grid-template-rows: 280px 220px 220px;
      }

      .gallery-card:first-child {
        grid-column: auto;
      }

      .footer-inner {
        flex-direction: column;
        align-items: flex-start;
      }

      .brand strong {
        font-size: .76rem;
      }

      .brand small {
        font-size: .52rem;
      }
    }
  </style>
</head>

<body>

  <!-- NAVIGATION -->

  <header class="nav">
    <div class="container nav-inner">

      <a class="brand" href="#home">
        <span class="crest">UN</span>

        <span>
          <small>St. Laurence High School</small>
          <strong>MODEL UNITED NATIONS</strong>
        </span>
      </a>

      <nav class="nav-links">
        <a href="#about">About</a>
        <a href="#mun">What is MUN?</a>
        <a href="#conferences">Conferences</a>
        <a href="#meetings">Meetings</a>
        <a href="#team">Team</a>
        <a href="#contact">Contact</a>
      </nav>

      <a
        class="btn btn-gold"
        href="https://linktr.ee/stl_mun?utm_source=linktree_profile_share&ltsid=fada2912-4ddf-4089-8ad4-9672580ae966"
        target="_blank">
        Linktree ↗
      </a>

      <button
        class="menu"
        aria-label="Open navigation"
        onclick="document.querySelector('.nav-links').classList.toggle('open')">
        ☰
      </button>

    </div>
  </header>


  <main>

    <!-- HERO -->

    <section class="hero" id="home">

      <div class="container hero-grid">

        <div>

          <span class="eyebrow">
            STLMUN · Burbank, Illinois
          </span>

          <h1>
            Where students
            <span>represent the world.</span>
          </h1>

          <p class="hero-lead">
            St. Laurence High School Model United Nations is a student-led
            team focused on diplomacy, debate, research, public speaking,
            and global affairs through competitive conferences and
            collaborative preparation.
          </p>

          <div class="hero-actions">

            <a class="btn btn-gold" href="#about">
              Explore STLMUN
            </a>

            <a
              class="btn"
              style="border:1px solid rgba(255,255,255,.3);color:white;"
              href="https://www.instagram.com/stl_mun/"
              target="_blank">
              Instagram ↗
            </a>

          </div>

          <p class="hero-location">
            A St. Laurence High School student organization · @stlaurencevikes
          </p>

        </div>


        <div class="hero-photo">

          <img
            src="assets/hero.jpg"
            alt="St. Laurence Model UN display with flags and gavel">

          <div class="photo-tag">
            Diplomacy · Debate · Global Affairs
          </div>

        </div>

      </div>

    </section>


    <!-- ABOUT / MISSION -->

    <section class="about" id="about">

      <div class="container">

        <div class="section-head">

          <div>
            <span class="eyebrow">About STLMUN</span>
            <h2>Learning diplomacy by doing it.</h2>
          </div>

          <p>
            Model United Nations turns global issues into an interactive
            academic experience. At St. Laurence, delegates prepare to
            represent assigned nations, defend policy positions,
            negotiate with other delegations, and work toward practical
            resolutions.
          </p>

        </div>


        <div class="about-grid">

          <article class="about-card dark">

            <h3>Our Mission</h3>

            <p>
              To give St. Laurence students a meaningful space to engage
              with international issues, strengthen communication and
              research skills, and experience diplomacy through
              preparation, competition, collaboration, and leadership.
            </p>

          </article>


          <article class="about-card">

            <h3>Our Approach</h3>

            <p>
              STLMUN combines research with real-time debate. Students
              move from understanding an issue to building an argument,
              responding under pressure, negotiating across perspectives,
              and contributing to a collective solution.
            </p>

          </article>

        </div>

      </div>

    </section>


    <!-- WHAT IS MODEL UN -->

    <section class="mun" id="mun">

      <div class="container">

        <div class="section-head">

          <div>
            <span class="eyebrow">What is Model UN?</span>
            <h2>The gist of MUN.</h2>
          </div>

          <p>
            Delegates simulate the work of international diplomats.
            Each student is assigned a country or role and prepares
            from that perspective before entering committee sessions
            with other schools.
          </p>

        </div>


        <div class="steps">

          <article class="step" data-number="01">

            <span class="step-number">01 · RESEARCH</span>

            <h3>Know your country.</h3>

            <p>
              Study the issue, your country's policies, interests,
              allies, and priorities so your position is informed
              and defensible.
            </p>

          </article>


          <article class="step" data-number="02">

            <span class="step-number">02 · DEBATE</span>

            <h3>Take the floor.</h3>

            <p>
              Present arguments, respond to other delegates, ask
              questions, and participate in formal and informal
              caucusing.
            </p>

          </article>


          <article class="step" data-number="03">

            <span class="step-number">03 · NEGOTIATE</span>

            <h3>Build consensus.</h3>

            <p>
              Find common ground, form blocs, combine ideas, and
              work with other delegations to create stronger proposals.
            </p>

          </article>


          <article class="step" data-number="04">

            <span class="step-number">04 · RESOLVE</span>

            <h3>Write & vote.</h3>

            <p>
              Turn negotiations into resolution language, defend the
              final proposal, and participate in committee voting.
            </p>

          </article>

        </div>

      </div>

    </section>


    <!-- CONFERENCES -->

    <section class="conferences" id="conferences">

      <div class="container">

        <div class="section-head">

          <div>
            <span class="eyebrow">Conference Experience</span>
            <h2>From the classroom to committee.</h2>
          </div>

          <p>
            Conference days put research, speaking, negotiation,
            and teamwork into practice. STLMUN has participated in
            regional Model UN experiences and committee simulations,
            giving delegates opportunities to compete, collaborate,
            and represent their assigned nations.
          </p>

        </div>


        <div class="conference-grid">

          <div class="conference-photo">

            <img
              src="assets/conference.jpg"
              alt="St. Laurence Model UN delegates at a conference">

            <div class="caption">
              STLMUN delegates at a conference
            </div>

          </div>


          <div class="conference-list">

            <article class="conference-card">

              <span class="conference-meta">
                Conference Participation
              </span>

              <h3>CSMUN XXVI</h3>

              <p>
                STLMUN delegates have competed in CSMUN,
                developing experience with conference procedures,
                committee debate, collaboration, and delegate
                performance.
              </p>

            </article>


            <article class="conference-card">

              <span class="conference-meta">
                Conference Participation
              </span>

              <h3>ICPMUN '27</h3>

              <p>
                Delegates represented their assigned countries and
                participated in committee sessions, with STLMUN
                celebrating delegate recognition and strong
                conference participation.
              </p>

            </article>


            <article class="conference-card">

              <span class="conference-meta">
                Conference Participation
              </span>

              <h3>MUNAP XXI</h3>

              <p>
                Another conference experience represented in
                STLMUN's team history, giving students an opportunity
                to apply preparation and diplomacy skills in a
                competitive setting.
              </p>

            </article>


            <div class="recognition">

              <strong>Delegate recognition matters.</strong>

              <span>
                Recent STLMUN posts highlight an Honorable Mention
                for America Fernandez and an Honorable Delegate
                recognition for Sydney Shen in Chicago City Council.
              </span>

            </div>

          </div>

        </div>

      </div>

    </section>


    <!-- MEETINGS -->

    <section class="meetings" id="meetings">

      <div class="container">

        <div class="section-head">

          <div>
            <span class="eyebrow">Inside the Team</span>
            <h2>Preparation becomes performance.</h2>
          </div>

          <p>
            Strong conference performance starts before conference day.
            STLMUN meetings build the skills delegates need:
            research, speaking, parliamentary procedure, negotiation,
            and collaborative writing.
          </p>

        </div>


        <div class="meeting-grid">

          <div class="meeting-box">

            <h3>Meeting Structure</h3>

            <p>
              A typical STLMUN cycle can move from learning the format
              to preparing a position, practicing committee skills,
              and getting ready for a conference.
            </p>


            <div class="meeting-list">

              <div class="meeting-item">
                <i class="dot"></i>
                <div>
                  <strong>Briefing & Current Events</strong>
                  <span>
                    Build context around the issues being discussed.
                  </span>
                </div>
              </div>


              <div class="meeting-item">
                <i class="dot"></i>
                <div>
                  <strong>Country & Issue Research</strong>
                  <span>
                    Develop a position grounded in credible sources.
                  </span>
                </div>
              </div>


              <div class="meeting-item">
                <i class="dot"></i>
                <div>
                  <strong>Debate & Caucus Practice</strong>
                  <span>
                    Practice speeches, responses, negotiation,
                    and procedure.
                  </span>
                </div>
              </div>


              <div class="meeting-item">
                <i class="dot"></i>
                <div>
                  <strong>Resolution Writing</strong>
                  <span>
                    Translate ideas and negotiations into
                    structured proposals.
                  </span>
                </div>
              </div>


              <div class="meeting-item">
                <i class="dot"></i>
                <div>
                  <strong>Conference Preparation</strong>
                  <span>
                    Review strategy, committee expectations,
                    and delegate goals.
                  </span>
                </div>
              </div>

            </div>

          </div>


          <div class="contributions">

            <article class="contribution-card">

              <div class="contribution-number">01</div>

              <h3>Research</h3>

              <p>
                Investigate countries, policies, history,
                and current international issues.
              </p>

            </article>


            <article class="contribution-card">

              <div class="contribution-number">02</div>

              <h3>Public Speaking</h3>

              <p>
                Build confidence in speeches, moderated caucuses,
                and spontaneous responses.
              </p>

            </article>


            <article class="contribution-card">

              <div class="contribution-number">03</div>

              <h3>Collaboration</h3>

              <p>
                Work across different positions to find common
                ground and create solutions.
              </p>

            </article>


            <article class="contribution-card">

              <div class="contribution-number">04</div>

              <h3>Leadership</h3>

              <p>
                Take initiative in preparation, team culture,
                conference strategy, and communication.
              </p>

            </article>

          </div>

        </div>

      </div>

    </section>


    <!-- TEAM -->

    <section class="team" id="team">

      <div class="container team-grid">

        <div class="team-photo">

          <img
            src="assets/team.jpg"
            alt="St. Laurence Model UN students at a conference">

        </div>


        <div class="team-content">

          <span class="eyebrow">
            The STLMUN Team
          </span>

          <h2>
            A team built around curiosity,
            preparation, and perspective.
          </h2>

          <p>
            STLMUN is more than conference day. It is a student
            community where members learn from one another,
            practice together, represent different perspectives,
            and grow into more confident communicators.
          </p>


          <div class="leaders">

            <div class="leader">
              <strong>Arianna Ramos</strong>
              <span>President</span>
            </div>

            <div class="leader">
              <strong>Sydney Shen</strong>
              <span>Vice President</span>
            </div>

            <div class="leader">
              <strong>Natalia Kwak</strong>
              <span>Media Chair</span>
            </div>

          </div>


          <div class="impact">

            <div class="impact-card">
              <b>3+</b>
              <span>conference experiences highlighted</span>
            </div>

            <div class="impact-card">
              <b>∞</b>
              <span>perspectives brought to committee</span>
            </div>

            <div class="impact-card">
              <b>1</b>
              <span>STLMUN community</span>
            </div>

          </div>

        </div>

      </div>

    </section>


    <!-- GALLERY -->

    <section class="gallery">

      <div class="container">

        <div class="section-head">

          <div>
            <span class="eyebrow">STLMUN in Action</span>
            <h2>Beyond the podium.</h2>
          </div>

          <p>
            Conference rooms, team moments, research displays,
            and the people who make STLMUN a community.
          </p>

        </div>


        <div class="gallery-grid">

          <figure class="gallery-card">

            <img
              src="assets/hero.jpg"
              alt="STLMUN Model UN display with country flags and gavel">

            <figcaption class="gallery-label">
              Model UN Showcase
            </figcaption>

          </figure>


          <figure class="gallery-card">

            <img
              src="assets/conference.jpg"
              alt="STLMUN delegates at a conference">

            <figcaption class="gallery-label">
              Conference Day
            </figcaption>

          </figure>


          <figure class="gallery-card">

            <img
              src="assets/team.jpg"
              alt="STLMUN team">

            <figcaption class="gallery-label">
              The Team
            </figcaption>

          </figure>

        </div>

      </div>

    </section>


    <!-- FLAGS -->

    <section class="global">

      <div class="container">

        <div class="section-head">

          <div>
            <span class="eyebrow">Global Perspective</span>
            <h2>Many flags. One room.</h2>
          </div>

          <p>
            Model UN asks students to step outside their own
            perspective and represent the interests of another
            nation. Delegates research countries, policies,
            international relationships, and global issues.
          </p>

        </div>


        <div class="flags">

          <span class="flag"><span>🇲🇽</span>Mexico</span>
          <span class="flag"><span>🇧🇷</span>Brazil</span>
          <span class="flag"><span>🇩🇰</span>Denmark</span>
          <span class="flag"><span>🇵🇪</span>Peru</span>
          <span class="flag"><span>🇨🇴</span>Colombia</span>
          <span class="flag"><span>🇳🇬</span>Nigeria</span>
          <span class="flag"><span>🇰🇪</span>Kenya</span>
          <span class="flag"><span>🇿🇦</span>South Africa</span>
          <span class="flag"><span>🇪🇸</span>Spain</span>
          <span class="flag"><span>🇺🇳</span>United Nations</span>

        </div>

      </div>

    </section>


    <!-- CONTACT -->

    <section class="contact" id="contact">

      <div class="container contact-grid">

        <div class="contact-copy">

          <span class="eyebrow">
            Connect with STLMUN
          </span>

          <h2>
            Interested in Model UN?
          </h2>

          <p>
            Follow STLMUN for team announcements, conference
            updates, delegate highlights, meeting information,
            and opportunities to get involved.
          </p>


          <div class="contact-buttons">

            <a
              class="btn btn-dark"
              href="https://www.instagram.com/stl_mun/"
              target="_blank">
              @stl_mun on Instagram ↗
            </a>

            <a
              class="btn btn-gold"
              href="https://linktr.ee/stl_mun?utm_source=linktree_profile_share&ltsid=fada2912-4ddf-4089-8ad4-9672580ae966"
              target="_blank">
              Open Linktree ↗
            </a>

          </div>

        </div>


        <aside class="contact-card">

          <div class="contact-label">
            Media & Website
          </div>

          <a href="mailto:nkwak29@stlaurence.com">
            nkwak29@stlaurence.com
          </a>


          <div class="contact-label">
            Media Chair
          </div>

          <a href="mailto:nkwak29@stlaurence.com">
            Natalia Kwak
          </a>


          <div class="contact-label">
            St. Laurence High School
          </div>

          <a
            href="https://www.instagram.com/stlaurencevikes/"
            target="_blank">
            @stlaurencevikes ↗
          </a>

        </aside>

      </div>

    </section>

  </main>


  <!-- FOOTER -->

  <footer>

    <div class="container footer-inner">

      <p>
        <strong>STLMUN</strong>
        · St. Laurence High School Model United Nations
        · Burbank, IL
      </p>

      <div class="footer-links">

        <a
          href="https://www.instagram.com/stl_mun/"
          target="_blank">
          Instagram
        </a>

        <a
          href="https://linktr.ee/stl_mun?utm_source=linktree_profile_share&ltsid=fada2912-4ddf-4089-8ad4-9672580ae966"
          target="_blank">
          Linktree
        </a>

        <a
          href="https://www.instagram.com/stlaurencevikes/"
          target="_blank">
          @stlaurencevikes
        </a>

      </div>

    </div>

  </footer>


  <script>

    // Mobile navigation

    document.querySelectorAll(".nav-links a").forEach(link => {

      link.addEventListener("click", () => {

        document
          .querySelector(".nav-links")
          .classList.remove("open");

      });

    });

  </script>

</body>
</html>

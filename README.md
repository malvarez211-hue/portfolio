<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Maria C. Alvarez | MSW E-Portfolio</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,400;0,700;1,400;1,700&family=Raleway:wght@300;400;500;600&display=swap" rel="stylesheet">
<style>
  *, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
  html { scroll-behavior: smooth; }
  body { background: #1a2035; color: #d4cfc8; font-family: 'Raleway', sans-serif; font-weight: 300; line-height: 1.7; }

  nav { position: fixed; top: 0; left: 0; right: 0; z-index: 100; background: #1a2035; border-bottom: 1px solid rgba(201,169,110,0.2); padding: 0 4rem; display: flex; align-items: center; justify-content: space-between; height: 64px; }
  .nav-name { font-family: 'Playfair Display', serif; font-size: 17px; font-style: italic; color: #c9a84c; letter-spacing: 1px; }
  .nav-links { display: flex; gap: 2rem; list-style: none; }
  .nav-links a { font-size: 10px; letter-spacing: 3px; text-transform: uppercase; color: #d4cfc8; text-decoration: none; transition: color 0.2s; }
  .nav-links a:hover { color: #c9a84c; }

  .hero { min-height: 100vh; display: flex; flex-direction: column; align-items: center; justify-content: center; text-align: center; padding: 8rem 2rem 5rem; background: #1a2035; position: relative; overflow: hidden; }
  .hero::after { content: ''; position: absolute; bottom: 0; left: 0; right: 0; height: 1px; background: linear-gradient(90deg, transparent, #c9a84c, transparent); }
  .hero-badge { font-size: 10px; letter-spacing: 5px; text-transform: uppercase; color: #c9a84c; margin-bottom: 3rem; }
  .hero h1 { font-family: 'Playfair Display', serif; font-size: clamp(56px, 10vw, 100px); font-weight: 400; line-height: 1.0; color: #ffffff; margin-bottom: 0.5rem; }
  .hero h1 em { font-style: italic; color: #c9a84c; }
  .hero-rule { width: 80px; height: 1px; background: linear-gradient(90deg, transparent, #c9a84c, transparent); margin: 1.5rem auto; }
  .hero-sub { font-size: 11px; letter-spacing: 4px; text-transform: uppercase; color: #c9a84c; margin-bottom: 2.5rem; }
  .hero-bio { max-width: 580px; font-size: 15px; color: #d4cfc8; line-height: 1.95; margin-bottom: 3rem; }
  .hero-tags { display: flex; flex-wrap: wrap; gap: 10px; justify-content: center; }
  .htag { font-size: 10px; letter-spacing: 2px; text-transform: uppercase; padding: 6px 16px; border: 1px solid #c9a84c; color: #c9a84c; }

  .section-wrap { padding: 6rem 4rem; max-width: 1200px; margin: 0 auto; }
  .section-eyebrow { font-size: 10px; letter-spacing: 5px; text-transform: uppercase; color: #c9a84c; margin-bottom: 0.75rem; display: flex; align-items: center; gap: 12px; }
  .section-eyebrow::after { content: ''; flex: 0 0 40px; height: 1px; background: #c9a84c; }
  .section-title { font-family: 'Playfair Display', serif; font-size: clamp(32px, 4vw, 52px); font-weight: 400; color: #ffffff; margin-bottom: 3rem; line-height: 1.1; }
  .section-title em { font-style: italic; color: #c9a84c; }
  .full-divider { width: 100%; height: 1px; background: rgba(201,169,110,0.15); }

  .about-grid { display: grid; grid-template-columns: 1.2fr 1fr; gap: 5rem; align-items: start; }
  .about-text p { font-size: 15px; color: #d4cfc8; line-height: 1.95; margin-bottom: 1.25rem; }
  .values-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 16px; }
  .value-card { background: #1f2a45; padding: 1.75rem; position: relative; overflow: hidden; border-radius: 8px; }
  .value-card::before { content: ''; position: absolute; top: 0; left: 0; right: 0; height: 2px; background: linear-gradient(90deg, #c9a84c, transparent); }
  .value-card h4 { font-size: 10px; letter-spacing: 2px; text-transform: uppercase; color: #c9a84c; margin-bottom: 10px; font-weight: 400; }
  .value-card p { font-size: 12px; color: #b0a898; line-height: 1.7; }

  .prose-text p { font-size: 15px; color: #d4cfc8; line-height: 1.95; margin-bottom: 1.25rem; }
  .prose-text p:last-child { margin-bottom: 0; }

  .comp-intro { font-size: 15px; color: #b0a898; margin-bottom: 3rem; line-height: 1.85; max-width: 650px; }
  .comp-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 16px; }
  .comp-card { background: #1f2a45; padding: 2.25rem; position: relative; overflow: hidden; transition: background 0.3s; border-radius: 8px; }
  .comp-card::before { content: ''; position: absolute; top: 0; left: 0; right: 0; height: 2px; background: linear-gradient(90deg, #c9a84c, transparent); }
  .comp-card:hover { background: #c9a84c; }
  .comp-card:hover .comp-num, .comp-card:hover .comp-title, .comp-card:hover .comp-desc { color: #1a2035; }
  .comp-card:hover .comp-num { opacity: 1; }
  .comp-num { font-family: 'Playfair Display', serif; font-size: 48px; font-weight: 400; font-style: italic; color: #c9a84c; opacity: 0.7; margin-bottom: 12px; line-height: 1; transition: all 0.3s; }
  .comp-title { font-size: 13px; font-weight: 600; color: #ffffff; margin-bottom: 10px; line-height: 1.35; letter-spacing: 0.5px; transition: color 0.3s; text-transform: uppercase; }
  .comp-desc { font-size: 12px; color: #b0a898; line-height: 1.7; font-weight: 300; transition: color 0.3s; }

  .kle-intro { font-size: 15px; color: #b0a898; margin-bottom: 3rem; line-height: 1.85; max-width: 700px; }
  .kle-list { display: grid; gap: 24px; }
  .kle-card { background: #1f2a45; border: 1px solid rgba(201,169,110,0.2); border-left: 3px solid #c9a84c; border-radius: 8px; padding: 2.5rem; }
  .kle-header { display: flex; align-items: flex-start; justify-content: space-between; flex-wrap: wrap; gap: 1rem; margin-bottom: 1.5rem; }
  .kle-badge { font-size: 10px; letter-spacing: 2px; text-transform: uppercase; color: #c9a84c; background: rgba(201,169,110,0.1); border: 1px solid rgba(201,169,110,0.3); padding: 4px 12px; border-radius: 3px; }
  .kle-score { font-size: 13px; color: #c9a84c; font-weight: 600; }
  .kle-course { font-size: 10px; letter-spacing: 2px; text-transform: uppercase; color: #b0a898; margin-bottom: 6px; }
  .kle-title { font-family: 'Playfair Display', serif; font-size: 22px; color: #ffffff; font-weight: 400; margin-bottom: 8px; }
  .kle-comps { font-size: 11px; color: #c9a84c; letter-spacing: 1px; margin-bottom: 1.25rem; }
  .kle-label { font-size: 10px; letter-spacing: 2px; text-transform: uppercase; color: #c9a84c; margin-bottom: 6px; margin-top: 1rem; }
  .kle-narrative { font-size: 14px; color: #d4cfc8; line-height: 1.85; }
  .kle-why { font-size: 13px; color: #b0a898; line-height: 1.75; font-style: italic; margin-top: 0.5rem; }

  .resume-intro { font-size: 15px; color: #b0a898; line-height: 1.85; margin-bottom: 3rem; max-width: 700px; }
  .dmh-award { background: linear-gradient(135deg, #1f2a45, #1a2035); border: 1px solid #c9a84c; border-radius: 8px; padding: 2rem 2.5rem; display: flex; align-items: center; gap: 2rem; margin-bottom: 3rem; flex-wrap: wrap; }
  .dmh-icon { font-size: 2.5rem; }
  .dmh-text h3 { font-family: 'Playfair Display', serif; font-size: 20px; color: #c9a84c; margin-bottom: 4px; }
  .dmh-text p { font-size: 13px; color: #b0a898; line-height: 1.6; }
  .dmh-amount { margin-left: auto; text-align: right; }
  .dmh-amount span { display: block; font-family: 'Playfair Display', serif; font-size: 28px; color: #c9a84c; font-style: italic; }
  .dmh-amount small { font-size: 11px; color: #b0a898; letter-spacing: 1px; }
  .resume-section-title { font-size: 10px; letter-spacing: 4px; text-transform: uppercase; color: #c9a84c; margin-bottom: 1.25rem; padding-bottom: 8px; border-bottom: 1px solid rgba(201,169,110,0.2); }
  .exp-list { display: grid; gap: 20px; margin-bottom: 3rem; }
  .exp-card { background: #1f2a45; border: 1px solid rgba(201,169,110,0.2); border-left: 2px solid #c9a84c; padding: 2rem 2.5rem; display: grid; grid-template-columns: 220px 1fr; gap: 3rem; align-items: start; border-radius: 8px; transition: border-color 0.2s; }
  .exp-card:hover { border-color: #c9a84c; }
  .exp-org { font-size: 10px; letter-spacing: 2px; text-transform: uppercase; color: #c9a84c; margin-bottom: 8px; }
  .exp-title { font-family: 'Playfair Display', serif; font-size: 18px; font-weight: 400; color: #ffffff; margin-bottom: 8px; line-height: 1.3; }
  .exp-date { font-size: 10px; letter-spacing: 1px; color: #c9a84c; text-transform: uppercase; border: 1px solid rgba(201,169,110,0.3); display: inline-block; padding: 3px 10px; }
  .exp-bullets { font-size: 13px; color: #b0a898; line-height: 1.85; padding-left: 1rem; }
  .exp-bullets li { margin-bottom: 0.4rem; }
  .edu-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 16px; margin-bottom: 3rem; }
  .edu-card { background: #1f2a45; border: 1px solid rgba(201,169,110,0.15); border-radius: 8px; padding: 1.75rem; }
  .edu-card h4 { font-family: 'Playfair Display', serif; font-size: 16px; color: #ffffff; margin-bottom: 6px; font-weight: 400; }
  .edu-card p { font-size: 12px; color: #b0a898; line-height: 1.6; }
  .edu-date { font-size: 11px; color: #c9a84c; margin-top: 8px; letter-spacing: 1px; display: block; }

  .skills-grid { display: grid; grid-template-columns: repeat(3, 1fr); gap: 16px; }
  .skill-card { background: #1f2a45; border: 1px solid rgba(201,169,110,0.2); padding: 2rem; transition: border-color 0.2s; border-radius: 8px; }
  .skill-card:hover { border-color: #c9a84c; }
  .skill-card h4 { font-size: 10px; letter-spacing: 3px; text-transform: uppercase; color: #c9a84c; margin-bottom: 1.25rem; font-weight: 400; padding-bottom: 10px; border-bottom: 1px solid rgba(201,169,110,0.2); }
  .skill-tag { display: inline-block; font-size: 11px; color: #d4cfc8; background: rgba(255,255,255,0.05); padding: 4px 10px; margin: 3px 3px 3px 0; letter-spacing: 0.5px; border-radius: 3px; }

  .contact-inner { text-align: center; padding: 2rem 0; }
  .contact-inner p { font-size: 15px; color: #d4cfc8; margin-bottom: 8px; }
  .contact-inner strong { color: #c9a84c; font-weight: 400; }

  footer { text-align: center; padding: 2.5rem; background: #141928; border-top: 1px solid rgba(201,169,110,0.15); }
  footer p { font-size: 10px; color: #8a8898; letter-spacing: 3px; text-transform: uppercase; }

  @media (max-width: 768px) {
    nav { padding: 0 1.5rem; }
    .section-wrap { padding: 4rem 1.5rem; }
    .about-grid, .values-grid, .comp-grid, .skills-grid, .edu-grid { grid-template-columns: 1fr; }
    .exp-card { grid-template-columns: 1fr; gap: 1rem; }
    .dmh-award { flex-direction: column; }
    .dmh-amount { margin-left: 0; text-align: left; }
    .nav-links { display: none; }
  }
</style>
</head>
<body>

<nav>
  <div class="nav-name">Maria C. Alvarez</div>
  <ul class="nav-links">
    <li><a href="#about">About</a></li>
    <li><a href="#philosophy">Philosophy</a></li>
    <li><a href="#specialization">Specialization</a></li>
    <li><a href="#competencies">Competencies</a></li>
    <li><a href="#kle">Key Learning</a></li>
    <li><a href="#resume">Resume</a></li>
    <li><a href="#contact">Contact</a></li>
  </ul>
</nav>

<!-- HERO -->
<div class="hero">
  <p class="hero-badge">MSW E-Portfolio</p>
  <h1>Maria C. <em>Alvarez</em></h1>
  <div class="hero-rule"></div>
  <p class="hero-sub">MSW Graduate · Clinical Mental Health Social Work · CSUDH</p>
  <p class="hero-bio">A bilingual, community-rooted social worker committed to trauma-informed, culturally responsive, and equity-centered practice. Graduated May 2026.</p>
  <div class="hero-tags">
    <span class="htag">Clinical Mental Health</span>
    <span class="htag">Bilingual EN/ES</span>
    <span class="htag">CRT Framework</span>
    <span class="htag">Community Practice</span>
    <span class="htag">CSUDH MSW 2026</span>
  </div>
</div>

<div class="full-divider"></div>

<!-- ABOUT -->
<div id="about" class="section-wrap">
  <p class="section-eyebrow">Who I Am</p>
  <h2 class="section-title">About <em>Me</em></h2>
  <div class="about-grid">
    <div class="about-text">
      <p>My name is Maria C. Alvarez and I am a bilingual (English/Spanish) Master of Social Work candidate at California State University, Dominguez Hills, graduating May 2026. I was born and raised in the Los Angeles area, and my roots in this community are at the heart of everything I do as a social worker.</p>
      <p>My practice is grounded in a deep commitment to equity, social justice, and culturally responsive care. I have worked with diverse populations across community health, mental health, and aging services settings — always centering the voices, strengths, and lived experiences of the people I serve.</p>
      <p>I am passionate about addressing the systemic barriers that prevent marginalized communities from accessing the resources and care they deserve. Whether in direct practice or macro-level advocacy, I bring a Critical Race Theory lens, trauma-informed approach, and genuine dedication to my work.</p>
    </div>
    <div class="values-grid">
      <div class="value-card"><h4>Social Justice</h4><p>Committed to dismantling systemic inequities and advocating for the rights and dignity of all people.</p></div>
      <div class="value-card"><h4>Cultural Humility</h4><p>Continuously learning and growing in my ability to honor and affirm the diverse identities of those I serve.</p></div>
      <div class="value-card"><h4>Trauma-Informed Practice</h4><p>Meeting every client with compassion, safety, and an understanding of how trauma shapes lived experience.</p></div>
      <div class="value-card"><h4>Community Empowerment</h4><p>Believing that lasting change happens when communities lead — centering their voices in every solution.</p></div>
    </div>
  </div>
</div>

<div class="full-divider"></div>

<!-- PROFESSIONAL PHILOSOPHY -->
<div id="philosophy" class="section-wrap">
  <p class="section-eyebrow">My Foundation</p>
  <h2 class="section-title">Professional <em>Philosophy</em></h2>
  <div class="prose-text">
    <p>I believe that healing is not a linear process, and that every person who walks through my door carries a story shaped by forces far greater than themselves. My practice is grounded in the conviction that effective social work requires us to look beyond the presenting problem and toward the systems, histories, and lived experiences that give it meaning. I approach every client relationship with curiosity, humility, and a deep respect for the resilience people carry — often without recognizing it themselves.</p>
    <p>My clinical philosophy is trauma-informed at its core. I understand that many of the behaviors and symptoms we see in community mental health settings are adaptations to pain, not character flaws or deficits. This shapes how I engage with clients — not as problems to be fixed, but as whole people navigating real and often unjust circumstances. I draw from strengths-based and anti-oppressive frameworks to ensure that my practice actively challenges the structural inequalities that contribute to mental health disparities, particularly within Latinx and other marginalized communities.</p>
    <p>As a bilingual clinician, I am committed to providing culturally responsive care that honors language not just as a tool for communication, but as an expression of identity, belonging, and trust. I believe that when clients are met in their full humanity — including their culture, their language, and their community — the therapeutic relationship becomes a space for genuine transformation.</p>
  </div>
</div>

<div class="full-divider"></div>

<!-- SPECIALIZATION STATEMENT -->
<div id="specialization" class="section-wrap">
  <p class="section-eyebrow">My Focus</p>
  <h2 class="section-title">Specialization <em>Statement</em></h2>
  <div class="prose-text">
    <p>My specialization in Community Mental Health reflects a deliberate commitment to serving adults with serious mental illness in settings where the need is great and the resources are often limited. Through my clinical internship at Rio Hondo Mental Health Clinic, I developed direct practice skills in assessment, diagnostic formulation, treatment planning, and individual therapy with a diverse adult population navigating conditions such as depression, anxiety, trauma, and psychosis. I applied evidence-based tools including the PHQ-9, GAD-7, and biopsychosocial assessments to inform care that is both clinically sound and person-centered.</p>
    <p>My training has prepared me to work at the intersection of mental health, social determinants, and systemic inequity. I apply Critical Race Theory as a lens for understanding how race, class, and institutional barriers shape mental health outcomes — and how clinicians can respond in ways that are affirming rather than retraumatizing. My work at WLCAC's Department of Family Services further deepened my understanding of the family and community systems that surround individual clients, reinforcing my belief that effective community mental health practice must extend beyond the therapy room.</p>
    <p>I am committed to growing as a bilingual, culturally competent clinician who centers equity, dignity, and self-determination in every aspect of practice. My goal is to contribute to a mental health landscape where communities that have historically been underserved receive not just access to care, but care that truly sees them.</p>
  </div>
</div>

<div class="full-divider"></div>

<!-- COMPETENCIES -->
<div id="competencies" class="section-wrap">
  <p class="section-eyebrow">CSWE Standards</p>
  <h2 class="section-title">9 Social Work <em>Competencies</em></h2>
  <p class="comp-intro">The following nine CSWE competencies are demonstrated through three key learning experiences completed in the Master of Social Work program at CSUDH.</p>
  <div class="comp-grid">
    <div class="comp-card"><div class="comp-num">01</div><p class="comp-title">Ethical & Professional Behavior</p><p class="comp-desc">Demonstrated through ethical decision-making in crisis situations, transparency with clients, and NASW Code of Ethics application.</p></div>
    <div class="comp-card"><div class="comp-num">02</div><p class="comp-title">Engage Diversity & Difference</p><p class="comp-desc">Applied through recovery-oriented, culturally responsive practice honoring each client's unique identity and social context.</p></div>
    <div class="comp-card"><div class="comp-num">03</div><p class="comp-title">Advance Human Rights & Justice</p><p class="comp-desc">Addressed systemic inequities through PAR research and CRT-informed practice in underserved communities.</p></div>
    <div class="comp-card"><div class="comp-num">04</div><p class="comp-title">Practice-Informed Research</p><p class="comp-desc">Designed a PAR proposal integrating community perspectives into research grounded in both evidence and lived experience.</p></div>
    <div class="comp-card"><div class="comp-num">05</div><p class="comp-title">Engage in Policy Practice</p><p class="comp-desc">Analyzed social policies affecting mental health and recovery, identifying structural barriers limiting access for marginalized populations.</p></div>
    <div class="comp-card"><div class="comp-num">06</div><p class="comp-title">Engage Individuals & Communities</p><p class="comp-desc">Applied developmental frameworks to engage clients across life stages with tailored, strengths-based communication strategies.</p></div>
    <div class="comp-card"><div class="comp-num">07</div><p class="comp-title">Assess Individuals & Families</p><p class="comp-desc">Conducted biopsychosocial and risk assessments informed by developmental theory and ecological systems frameworks.</p></div>
    <div class="comp-card"><div class="comp-num">08</div><p class="comp-title">Intervene with Individuals & Families</p><p class="comp-desc">Applied evidence-based interventions grounded in human development theory to support client growth across the lifespan.</p></div>
    <div class="comp-card"><div class="comp-num">09</div><p class="comp-title">Evaluate Practice</p><p class="comp-desc">Evaluated outcomes of micro and macro interventions using research-informed frameworks, reflecting critically on practice effectiveness.</p></div>
  </div>
</div>

<div class="full-divider"></div>

<!-- KEY LEARNING EXPERIENCES -->
<div id="kle" class="section-wrap">
  <p class="section-eyebrow">Academic Excellence</p>
  <h2 class="section-title">Key Learning <em>Experiences</em></h2>
  <p class="kle-intro">The following three assignments demonstrate proficiency across all nine CSWE social work competencies, completed during the Master of Social Work program at California State University, Dominguez Hills.</p>
  <div class="kle-list">

    <div class="kle-card">
      <div class="kle-header">
        <div>
          <p class="kle-course">MSW 531 — Research Methods</p>
          <h3 class="kle-title">Participatory Action Research Proposal</h3>
          <p class="kle-comps">Competencies: 1, 3, 4, 6, 9</p>
        </div>
        <div style="text-align:right;">
          <span class="kle-badge">KLE 1</span><br><br>
          <span class="kle-score">⭐ 25/25</span>
        </div>
      </div>
      <p class="kle-label">Reflective Narrative</p>
      <p class="kle-narrative">I chose this assignment because it demonstrates my ability to use research to understand community issues and support social change. This project helped me strengthen my skills in research-informed practice and ethical decision-making. Designing a CPAR proposal around illegal trash dumping in South Central LA pushed me to think beyond the individual and consider how systemic racism and environmental inequity intersect. It also challenged me to center community voices as co-researchers rather than subjects, which deepened my understanding of participatory justice and my own role as an advocate.</p>
      <p class="kle-label">Why I Included This</p>
      <p class="kle-why">This assignment showcases my ability to integrate CRT, environmental justice frameworks, and community-based research methods — skills central to macro social work practice.</p>
    </div>

    <div class="kle-card">
      <div class="kle-header">
        <div>
          <p class="kle-course">MSW 582 — Mental Health Practice</p>
          <h3 class="kle-title">Recovery Narrative Paper Part 2</h3>
          <p class="kle-comps">Competencies: 1, 2, 5, 9</p>
        </div>
        <div style="text-align:right;">
          <span class="kle-badge">KLE 2</span><br><br>
          <span class="kle-score">⭐ 92/100</span>
        </div>
      </div>
      <p class="kle-label">Reflective Narrative</p>
      <p class="kle-narrative">I chose this assignment because it demonstrates my understanding of how trauma and social support influence recovery. It also reflects my ability to analyze research and consider the cultural and systemic factors that affect mental health. Writing this paper challenged me to examine recovery not as a linear process but as something shaped by identity, community, and access to resources. It reinforced my commitment to providing culturally responsive, trauma-informed care — and reminded me why representation and lived experience matter in clinical practice.</p>
      <p class="kle-label">Why I Included This</p>
      <p class="kle-why">This paper highlights my ability to connect research, policy, and cultural competency to real clinical practice — demonstrating depth in both micro and macro perspectives.</p>
    </div>

    <div class="kle-card">
      <div class="kle-header">
        <div>
          <p class="kle-course">MSW 500 — Human Development</p>
          <h3 class="kle-title">Development Theory Paper</h3>
          <p class="kle-comps">Competencies: 4, 6, 7, 8</p>
        </div>
        <div style="text-align:right;">
          <span class="kle-badge">KLE 3</span><br><br>
          <span class="kle-score">⭐ 37/40</span>
        </div>
      </div>
      <p class="kle-label">Reflective Narrative</p>
      <p class="kle-narrative">I chose this assignment because it demonstrates my understanding of human development theories and how they guide social work assessment and intervention with clients. Engaging with multiple theoretical frameworks — from Erikson to ecological systems theory — helped me see how development is never just biological but deeply shaped by environment, culture, and social context. This paper strengthened my ability to meet clients where they are developmentally and to tailor my approach based on the unique life stage challenges each person faces.</p>
      <p class="kle-label">Why I Included This</p>
      <p class="kle-why">This assignment demonstrates my theoretical foundation in human development and my ability to apply multiple frameworks to assessment and intervention — core competencies for direct practice.</p>
    </div>

  </div>
</div>

<div class="full-divider"></div>

<!-- RESUME -->
<div id="resume" class="section-wrap">
  <p class="section-eyebrow">Curriculum Vitae</p>
  <h2 class="section-title">Resume</h2>
  <p class="resume-intro">Bilingual (English/Spanish) clinical social work graduate and MSW Graduate at California State University, Dominguez Hills. Dedicated to trauma-informed, culturally responsive, and equity-centered practice. Brings strong clinical skills in individual therapy, biopsychosocial assessment, crisis intervention, and case management. LA County DMH Graduate Stipend Award recipient committed to public mental health service in underserved communities.</p>

  <div class="dmh-award">
    <div class="dmh-icon">🏆</div>
    <div class="dmh-text">
      <h3>DMH Stipend Award Recipient</h3>
      <p>LA County Department of Mental Health Graduate Stipend · 2025–2026<br>Awarded to select MSW students demonstrating commitment to public mental health. Requires one year of post-graduation employment at a DMH-operated or contracted agency.</p>
    </div>
    <div class="dmh-amount">
      <span>$18,500</span>
      <small>Award Amount</small>
    </div>
  </div>

  <p class="resume-section-title">Work Experience</p>
  <div class="exp-list">
    <div class="exp-card">
      <div><p class="exp-org">Rio Hondo Mental Health Clinic · Cerritos, CA</p><p class="exp-title">Clinical Social Work Intern</p><p class="exp-date">09/2025 – 05/2026</p></div>
      <ul class="exp-bullets">
        <li>Conduct weekly 60-minute individual therapy sessions for a caseload of 5 adult clients, addressing emotional regulation, coping skills, and treatment goals.</li>
        <li>Conduct 3 comprehensive intake assessments per week (2 hours each) in the Triage Department, completing biopsychosocial evaluations and determining appropriate level of care.</li>
        <li>Conduct 50-minute telehealth sessions based on client needs, ensuring continuity and accessibility of services.</li>
        <li>Complete timely clinical documentation including progress notes (GIRP format) and comprehensive adult assessments in the electronic health record.</li>
        <li>Collaborate with multidisciplinary teams to support treatment planning, care coordination, and service linkage.</li>
        <li>Coordinate care by ensuring clients are scheduled for psychiatric appointments for medication evaluation and management.</li>
        <li>Assist in connecting clients to community resources and mental health services to support stabilization and ongoing care.</li>
      </ul>
    </div>
    <div class="exp-card">
      <div><p class="exp-org">California AHEC Scholars Program · Los Angeles, CA</p><p class="exp-title">Scholar & Intern</p><p class="exp-date">10/2024 – 06/2026</p></div>
      <ul class="exp-bullets">
        <li>Completed 9 online didactic modules focused on primary care systems, community health, and health workforce development including Team-Based Care, Patient Engagement, Quality Improvement, Community Engagement, and Leadership & Advocacy.</li>
        <li>Completed 9 online clinical case studies applying evidence-based reasoning to conditions including Hypertension, Diabetes, Depression, Asthma, COPD, and Culturally Responsive Care for Hispanic Patients.</li>
        <li>Designed and implemented a Personal Leadership Strategy for a Community-Based Health Project, engaging community members, clinic staff, and organizational partners to identify and address community health needs.</li>
        <li>Developed competencies in patient-centered care, interprofessional collaboration, community health advocacy, and cultural competency.</li>
      </ul>
    </div>
    <div class="exp-card">
      <div><p class="exp-org">KIPP Charter Schools · Los Angeles, CA</p><p class="exp-title">School Counselor Intern</p><p class="exp-date">08/2024 – 05/2025</p></div>
      <ul class="exp-bullets">
        <li>Facilitated weekly 45-minute group counseling sessions for 3 middle school students, focusing on emotional regulation, peer relationships, and coping skills.</li>
        <li>Provided individual counseling to 4 elementary students weekly (30-minute sessions) to support emotional development and behavioral needs.</li>
        <li>Delivered on-demand crisis and emotional support to students, responding to immediate needs and promoting a safe and supportive school environment.</li>
        <li>Collaborated with educators to identify at-risk students and coordinate appropriate interventions and follow-up support.</li>
      </ul>
    </div>
    <div class="exp-card">
      <div><p class="exp-org">WLCAC Department of Family Services · Los Angeles, CA</p><p class="exp-title">Community Health Worker</p><p class="exp-date">01/2023 – 08/2024</p></div>
      <ul class="exp-bullets">
        <li>Conducted 1–2 hour comprehensive assessments and developed individualized care plans for a caseload of 30 clients.</li>
        <li>Met with clients monthly to monitor progress, reinforce accountability, and ensure compliance with program expectations and court-mandated services.</li>
        <li>Collaborated with multidisciplinary teams (clinicians, case managers, and medical providers) to improve care coordination and client outcomes.</li>
        <li>Coordinated with parole officers and justice system stakeholders to track client progress and compliance with court-ordered treatment requirements.</li>
        <li>Facilitated referrals to community resources including housing, food assistance, and mental health services to support client stability.</li>
      </ul>
    </div>
    <div class="exp-card">
      <div><p class="exp-org">Casa Carmen Senior Home · Los Angeles, CA</p><p class="exp-title">Intern</p><p class="exp-date">08/2022 – 12/2022</p></div>
      <ul class="exp-bullets">
        <li>Supported 20–30 residents weekly with activities of daily living, medical appointment follow-ups, and medication coordination with pharmacies.</li>
        <li>Facilitated gentle yoga, light exercise, and outdoor activities to promote physical and emotional well-being.</li>
        <li>Created a monthly activity calendar to increase resident engagement and social interaction.</li>
      </ul>
    </div>
  </div>

  <p class="resume-section-title">Education</p>
  <div class="edu-grid">
    <div class="edu-card"><h4>Master of Social Work (MSW)</h4><p>California State University, Dominguez Hills</p><span class="edu-date">May 2026</span></div>
    <div class="edu-card"><h4>Bachelor of Arts in Human Services</h4><p>California State University, Dominguez Hills</p><span class="edu-date">May 2023</span></div>
    <div class="edu-card"><h4>Associate of Arts in Sociology</h4><p>Cerritos College</p><span class="edu-date">March 2021</span></div>
  </div>

  <p class="resume-section-title">Clinical Skills</p>
  <div class="skills-grid">
    <div class="skill-card"><h4>Clinical Practice</h4><span class="skill-tag">Individual Therapy</span><span class="skill-tag">Group Therapy</span><span class="skill-tag">Crisis Intervention</span><span class="skill-tag">Biopsychosocial Assessment</span><span class="skill-tag">Psychosocial Assessments</span><span class="skill-tag">Suicide Risk Assessment</span><span class="skill-tag">Safety Planning</span></div>
    <div class="skill-card"><h4>Documentation</h4><span class="skill-tag">GIRP Documentation</span><span class="skill-tag">Clinical Documentation</span><span class="skill-tag">Treatment Planning</span><span class="skill-tag">Case Management</span><span class="skill-tag">Care Coordination</span><span class="skill-tag">Telehealth Services</span></div>
    <div class="skill-card"><h4>Frameworks</h4><span class="skill-tag">Trauma-Informed Care</span><span class="skill-tag">Cognitive Behavioral Therapy (CBT)</span><span class="skill-tag">CRT Framework</span><span class="skill-tag">Strengths-Based Practice</span><span class="skill-tag">Cultural Humility</span><span class="skill-tag">Motivational Interviewing</span></div>
    <div class="skill-card"><h4>Populations</h4><span class="skill-tag">Adults with SMI</span><span class="skill-tag">Youth & Adolescents</span><span class="skill-tag">Justice-Involved</span><span class="skill-tag">Senior Care</span></div>
    <div class="skill-card"><h4>Languages</h4><span class="skill-tag">English (Fluent)</span><span class="skill-tag">Spanish (Fluent)</span></div>
    <div class="skill-card"><h4>Research & Advocacy</h4><span class="skill-tag">Participatory Action Research</span><span class="skill-tag">Evidence-Based Practice</span><span class="skill-tag">Community Health Advocacy</span><span class="skill-tag">Interprofessional Collaboration</span></div>
  </div>
</div>

<div class="full-divider"></div>

<!-- CONTACT -->
<div id="contact" class="section-wrap">
  <div class="contact-inner">
    <p class="section-eyebrow" style="justify-content:center;">Get In Touch</p>
    <h2 class="section-title" style="text-align:center;">Let's <em>Connect</em></h2>
    <p>Maria C. Alvarez &nbsp;·&nbsp; <strong>MSW Graduate</strong> &nbsp;·&nbsp; CSUDH</p>
    <p style="margin-top:8px;">Bilingual Clinical Social Work Graduate &nbsp;·&nbsp; Los Angeles, CA</p>
    <p style="margin-top:1.5rem; font-size:15px; color:#c9a84c;">conniealvarez007@gmail.com</p>
    <p style="margin-top:8px; font-size:15px; color:#c9a84c;">(562) 805-6150</p>
  </div>
</div>

<footer>
  <p>© 2026 Maria C. Alvarez · MSW E-Portfolio · CSUDH · Clinical Mental Health Social Work</p>
</footer>

</body>
</html>

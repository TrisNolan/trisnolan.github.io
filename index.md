---
layout: default
title: Home
---

<section class="hero" id="home" style="text-align: center;">
  <h1>Exploring the Microscopic Universe</h1>
  <p>Dive deep into the fascinating world of microbiology, where the smallest organisms hold the biggest secrets to life, health, and our planet's future.</p>
  <div class="dna-container">
    <div class="dna-helix">
      <div class="dna-strand"></div>
      <div class="dna-strand"></div>
      <div class="dna-strand"></div>
      <div class="dna-strand"></div>
    </div>
  </div>
  <div class="hero-image" style="margin-top: 2rem;">
    <img src="{{ '/assets/images/tristan-lab-cartoon.png' | relative_url }}" 
         alt="Tristan cartoon in lab" 
         style="max-width: 300px; width: 100%; border-radius: 10px; 
                box-shadow: 0 10px 30px rgba(100, 255, 218, 0.2); 
                display: block; margin-left: auto; margin-right: auto;">
  </div>
</section>

<!-- Wave divider -->
<div style="line-height:0;">
  <svg viewBox="0 0 1440 120" width="100%" height="120" preserveAspectRatio="none" aria-hidden="true">
    <path d="M0,60 C240,20 480,100 720,60 C960,20 1200,90 1440,50 L1440,120 L0,120 Z"
          fill="rgba(100,255,218,0.10)"></path>
    <path d="M0,60 C240,20 480,100 720,60 C960,20 1200,90 1440,50 L1440,120 L0,120 Z"
          fill="#64ffda"></path>
  </svg>
</div>

<section class="blog-section" id="blog">
  <h2 class="section-title">Latest Research & Insights</h2>
  <div class="blog-grid">
  {% for post in site.posts limit:8 %}
    <article class="blog-card">
      <h3><a href="{{ post.url | relative_url }}">{{ post.title }}</a></h3>
      <p>{{ post.excerpt | strip_html | truncate: 180 }}</p>
      <div class="blog-meta">{{ post.date | date: "%d %b %Y" }}</div>
    </article>
  {% endfor %}
  </div>
</section>

<!-- Microbe dots divider -->
<svg viewBox="0 0 1440 40" width="100%" height="40" preserveAspectRatio="none" aria-hidden="true"
     style="display:block; background:transparent;">
  <rect x="0" y="19" width="1440" height="2" fill="rgba(100,255,218,0.25)"></rect>
  <circle cx="80"  cy="20" r="3"  fill="#64ffda"/>
  <circle cx="210" cy="20" r="2.5" fill="#64ffda"/>
  <circle cx="340" cy="20" r="3.5" fill="#64ffda"/>
  <circle cx="470" cy="20" r="2.8" fill="#64ffda"/>
  <circle cx="600" cy="20" r="3.2" fill="#64ffda"/>
  <circle cx="730" cy="20" r="2.6" fill="#64ffda"/>
  <circle cx="860" cy="20" r="3.4" fill="#64ffda"/>
  <circle cx="990" cy="20" r="2.7" fill="#64ffda"/>
  <circle cx="1120" cy="20" r="3.1" fill="#64ffda"/>
  <circle cx="1250" cy="20" r="2.9" fill="#64ffda"/>
  <rect x="150" y="17" width="22" height="6" rx="3" fill="rgba(100,255,218,0.9)"/>
  <rect x="430" y="17" width="18" height="6" rx="3" fill="rgba(100,255,218,0.9)"/>
  <rect x="810" y="17" width="20" height="6" rx="3" fill="rgba(100,255,218,0.9)"/>
  <rect x="1190" y="17" width="24" height="6" rx="3" fill="rgba(100,255,218,0.9)"/>
</svg>

<section class="about-section" id="about">
  <h2 class="section-title">About Dr. Tristan Nolan</h2>
  <p>Welcome to my corner of the microbial world. I am an environmental microbiologist driven by a curiosity about how microorganisms influence ecosystems, health, and the environment. Since 2018, I have explored topics ranging from microbial ecology and water quality to the spread of antimicrobial resistance.</p>
  <br>
  <p>This blog is where I share ideas and insights, aiming to make the fascinating world of microbiology accessible to anyone with an interest in how microbes shape our lives.</p>

  <div style="margin-top: 1.5rem; text-align: center;">
    <a href="mailto:commoninscience.blog@outlook.com" 
       style="background: #64ffda; color: #0f0f23; padding: 0.8rem 1.5rem; 
              border-radius: 30px; text-decoration: none; font-weight: bold;">
      📧 Email Me
    </a>
  </div>
</section>

<section class="research-section" id="research">
  <h2 class="section-title">Research Publications</h2>
  <p style="text-align: center; max-width: 700px; margin: auto;">
    You can explore my full list of peer-reviewed publications, preprints, and conference contributions on my ResearchGate profile.
  </p>
  <div style="text-align: center; margin-top: 1.5rem;">
    <a href="https://www.researchgate.net/profile/Tristan-Nolan" target="_blank" 
       style="background: #64ffda; color: #0f0f23; padding: 0.8rem 1.5rem; border-radius: 30px; text-decoration: none; font-weight: bold;">
      View My ResearchGate Profile
    </a>
  </div>
</section>

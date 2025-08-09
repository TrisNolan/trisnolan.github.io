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

<!-- Animated wave divider -->
<div class="wave-divider">
  <svg viewBox="0 0 1440 120" xmlns="http://www.w3.org/2000/svg" preserveAspectRatio="none">
    <path fill="#64ffda" fill-opacity="0.8" d="M0,60 Q360,120 720,60 T1440,60 V120 H0 Z"></path>
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

<!-- Microbe of the Month Section -->
<section id="microbe-month" style="padding: 2rem 1rem; text-align: center;">
  <h2 class="section-title">🦠 Microbe of the Month</h2>
  <div id="microbe-card" style="background: rgba(100,255,218,0.05); border: 1px solid rgba(100,255,218,0.3); border-radius: 10px; max-width: 500px; margin: auto; padding: 1.5rem;">
    <a id="microbe-link" href="#" target="_blank" style="text-decoration: none; color: inherit;">
      <img id="microbe-img" src="" alt="Microbe image" style="max-width: 100%; border-radius: 8px; margin-bottom: 1rem;">
      <h3 id="microbe-name" style="color: #64ffda;"></h3>
      <p id="microbe-desc" style="line-height: 1.5;"></p>
    </a>
    <small id="microbe-source" style="color: rgba(255,255,255,0.6); display: block; margin-top: 0.5rem;"></small>
  </div>
</section>

<script>
  const microbes = [
    {
      name: "Deinococcus radiodurans",
      img: "https://upload.wikimedia.org/wikipedia/commons/0/0e/Deinococcus_radiodurans.png",
      desc: "Known as 'Conan the Bacterium', it can survive extreme radiation, cold, dehydration, and vacuum of space.",
      source: "Source: Wikipedia",
      link: "https://en.wikipedia.org/wiki/Deinococcus_radiodurans"
    },
    {
      name: "Vibrio fischeri",
      img: "https://upload.wikimedia.org/wikipedia/commons/8/82/Vibrio_fischeri.jpg",
      desc: "A bioluminescent marine bacterium that lives in symbiosis with certain squid species, helping them evade predators.",
      source: "Source: NOAA",
      link: "https://en.wikipedia.org/wiki/Vibrio_fischeri"
    },
    {
      name: "Bdellovibrio bacteriovorus",
      img: "https://upload.wikimedia.org/wikipedia/commons/0/0e/Bdellovibrio_bacteriovorus_TEM.jpg",
      desc: "A bacterial predator that invades and consumes other bacteria from the inside out.",
      source: "Source: Microbiology Society",
      link: "https://en.wikipedia.org/wiki/Bdellovibrio_bacteriovorus"
    }
  ];

  const monthIndex = new Date().getMonth() % microbes.length;
  const microbe = microbes[monthIndex];

  document.getElementById("microbe-name").textContent = microbe.name;
  document.getElementById("microbe-img").src = microbe.img;
  document.getElementById("microbe-desc").textContent = microbe.desc;
  document.getElementById("microbe-source").textContent = microbe.source;
  document.getElementById("microbe-link").href = microbe.link;
</script>

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

<style>
.wave-divider {
  position: relative;
  width: 100%;
  overflow: hidden;
  height: 60px;
  margin-bottom: -10px;
}
.wave-divider svg {
  width: 100%;
  height: 100%;
  animation: waveMove 8s ease-in-out infinite;
}
@keyframes waveMove {
  0% { transform: translateX(0); }
  50% { transform: translateX(-20px); }
  100% { transform: translateX(0); }
}
</style>

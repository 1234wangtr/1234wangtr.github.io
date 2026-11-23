---
layout: academic
permalink: /
redirect_from:
  - /about/
  - /about.html
---

<section class="hero" id="about" aria-labelledby="home-title">
  <div class="hero__intro">
    <p class="hero__native-name" lang="zh-Hans">{{ site.author.native_name | escape }}</p>
    <h1 id="home-title">{{ site.author.name | escape }}</h1>
    <p class="hero__role">PhD Student at {{ site.author.employer | escape }}</p>
    <p class="hero__bio">I study post-quantum cryptography at the <a href="https://www.insc.tsinghua.edu.cn/inscen/">Institute for Network Sciences and Cyberspace</a>. My research focuses on code-based cryptography and the security of constructions built from error-correcting codes.</p>
    <div class="hero__actions">
      <a class="academic-button" href="#publications">View publications</a>
      <a class="academic-button academic-button--outline" href="mailto:{{ site.author.email | escape }}">Email me</a>
    </div>
  </div>
  {% include code-matrix.html %}
</section>

<section class="home-section" id="research" aria-labelledby="research-title">
  <h2 id="research-title">Research interests</h2>
  <ul class="research-list" role="list">
    <li>
      <h3>Code-based cryptography</h3>
      <p>Design and security analysis of post-quantum cryptographic schemes built from error-correcting codes.</p>
    </li>
    <li>
      <h3>Syndrome decoding</h3>
      <p>Algorithms for structured decoding problems that underlie code-based security assumptions.</p>
    </li>
    <li>
      <h3>Pseudorandom codes</h3>
      <p>Security and privacy properties of pseudorandom and confidential error-correcting codes.</p>
    </li>
  </ul>
</section>

<section class="home-section" id="publications" aria-labelledby="publications-title">
  <div class="section-heading">
    <h2 id="publications-title">Publications</h2>
    <a class="text-link" href="{{ '/publications/' | relative_url }}">Browse by type</a>
  </div>
  {% assign publications = site.publications | sort: 'date' | reverse %}
  {% include publication-list.html publications=publications %}
</section>

<section class="home-section contact-section" id="contact" aria-labelledby="contact-title">
  <div>
    <h2 id="contact-title">Contact</h2>
    <p>{{ site.author.employer | escape }} · {{ site.author.location | escape }}</p>
  </div>
  <ul class="contact-links" role="list">
    <li><a href="mailto:{{ site.author.email | escape }}">{{ site.author.email | escape }}</a></li>
    <li><a href="{{ site.author.orcid | escape }}">ORCID</a></li>
    <li><a href="https://github.com/{{ site.author.github | escape }}">GitHub</a></li>
  </ul>
</section>

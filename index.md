---
layout: default
body_class: three-column
title: Home
---
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.4/css/all.min.css">
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/academicons@1.9.4/css/academicons.min.css">

<!-- Left: Image -->
<div class="left-column">
  <img src="{{ '/assets/imgs/me.jpg' | relative_url }}" alt="Profile">
</div>

<!-- Middle: Page content -->
<div class="middle-column">
  
    I'm a PhD candidate at the University of Amsterdam with <a href="https://sites.google.com/view/irisgroen" target="_blank">Iris I. A. Groen</a> and H. Steven Scholte.
        
    In my research, I leverage methods from Machine Learning, specifically Computer Vision, in combination with state-of-the-art neuroimaging techniques to study the underlying principles of human visual processing. I work in close collaboration with the Cognitive AI and Vision Amsterdam (CAVA) lab at the <a href="https://psyres.uva.nl/content/research-groups/programme-group-brain-and-cognition/programme-group-brain-and-cognition.html">Brain and Cognition Group Psychology Department</a>, <a href="https://ivi.fnwi.uva.nl/vislab/">the Video and Image Sense Lab (VISlab)</a> at the Informatics Institute, both at the University of Amsterdam. My project is embedded in and funded by the <a href="https://dsc.uva.nl/content/news/2021/10/seven-new-interdisciplinary-data-science-phd-positions.html">Interdisciplinary PhD Program of the UvA Data Science Center</a>.
        
    <p>Feel free to explore my <a href="/assets/files/Scientific_CV_NiklasMueller-EN.pdf" target="_blank">CV</a> or browse my <a href="publication_page">publications</a> and <a href="conference_presentation_page">conference presentations</a>.</p>

</div>

<!-- Right: Blog post headers -->
<div class="right-column">
  <h3>Recent Posts</h3>
  <ul>
    {%- assign posts = site.publications | sort: 'date' | reverse %}
    {% for post in posts reversed limit:3 %}
      <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
    {% endfor %}
    
    {%- assign posts = site.conference_presentations | sort: 'date' | reverse %}
    {% for post in posts limit:3 %}
      <li><a href="{{ post.url | relative_url }}">{{ post.title }}</a></li>
    {% endfor %}
  </ul>
</div>

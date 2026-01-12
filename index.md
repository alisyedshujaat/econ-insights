---
layout: home
title: Economic Insights
---

<header style="padding-bottom: 20px; border-bottom: 1px solid #eaecef; margin-bottom: 30px;">
  <h1 style="font-size: 2.5em; margin-bottom: 10px; color: #24292e;">Welcome to My Economics Platform</h1>
  <p style="font-size: 1.1em; line-height: 1.6; color: #586069;">
    I am <strong>Syed Shujaat Ali</strong>. This platform is dedicated to exploring the intersection of global economics, geopolitics, and market analysis. Through short articles and reviews, I aim to break down complex economic shifts and their real-world consequences.
  </p>
</header>

<section style="margin-bottom: 40px;">
  <h2 style="border-bottom: 2px solid #0366d6; display: inline-block; padding-bottom: 5px; margin-bottom: 25px;">Recent Articles</h2>
  
  <div style="display: flex; flex-direction: column; gap: 15px;">
    {% for post in site.posts %}
      <a href="{{ post.url | relative_url }}" style="text-decoration: none; color: inherit;">
        <div class="article-card" style="padding: 20px; border: 1px solid #e1e4e8; border-radius: 8px; background-color: #ffffff; transition: all 0.3s ease;">
          <h3 style="margin-top: 0; margin-bottom: 8px; color: #0366d6;">{{ post.title }}</h3>
          <p style="font-size: 0.9em; color: #6a737d; margin: 0;">📅 Published on {{ post.date | date: "%B %d, %Y" }}</p>
        </div>
      </a>
    {% endfor %}
  </div>
</section>

<section style="margin-top: 40px; padding: 25px; background-color: #f6f8fa; border-radius: 8px; border: 1px solid #e1e4e8;">
  <h2 style="margin-top: 0;">About the Project</h2>
  <p style="line-height: 1.6;">
    This platform is a dedicated space for transparent, data-driven economic analysis. By leveraging the open-source nature of GitHub, I aim to provide objective reviews and articles that demystify the complex shifts in our global and local economies.
  </p>
  
  <p style="font-weight: bold; margin-bottom: 10px;">My analysis focuses on three core pillars:</p>
  <ul style="line-height: 1.8;">
    <li><strong>Global Trends:</strong> Examining the forces shaping GDP growth, inflation, and trade stability.</li>
    <li><strong>Geopolitical Economy:</strong> Evaluating how international relations and policy decisions drive market outcomes.</li>
    <li><strong>Future Resilience:</strong> Exploring the impact of emerging technologies, energy transitions, and social shifts on long-term prosperity.</li>
  </ul>
  
  <p style="margin-top: 20px;"><strong>Contact:</strong> <a href="mailto:alisyedshujaat34@gmail.com" style="color: #0366d6; text-decoration: none; font-weight: bold;">alisyedshujaat34@gmail.com</a></p>
</section>

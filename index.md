---
layout: home
title: Economic Insights
---

<header style="padding-bottom: 20px; border-bottom: 1px solid #eaecef; margin-bottom: 30px;">
  <h1 style="font-size: 2.5em; margin-bottom: 10px; color: #24292e;">Economic Analysis Platform</h1>
  <p style="font-size: 1.1em; color: #586069;">Exploring global shifts in macroeconomics and geopolitics.</p>
</header>

<section style="margin-bottom: 40px;">
  <h2 style="border-bottom: 2px solid #0366d6; display: inline-block; padding-bottom: 5px; margin-bottom: 25px;">Explore Articles</h2>
  
  <input type="text" id="articleSearch" class="search-input" placeholder="🔍 Search by topic or category (e.g., Inflation, Venezuela, Energy)..." onkeyup="filterArticles()">

  <div id="articleContainer" style="display: flex; flex-direction: column; gap: 15px;">
    {% for post in site.posts %}
      <div class="article-item" data-title="{{ post.title | downcase }}" data-categories="{{ post.categories | join: ' ' | downcase }}">
        <a href="{{ post.url | relative_url }}" style="text-decoration: none; color: inherit;">
          <div class="article-card">
            <h3 style="margin-top: 0; margin-bottom: 8px; color: #0366d6;">{{ post.title }}</h3>
            <div style="display: flex; gap: 10px; align-items: center;">
               <span style="font-size: 0.85em; color: #6a737d;">📅 {{ post.date | date: "%B %d, %Y" }}</span>
               <span style="background: #f1f8ff; color: #0366d6; padding: 2px 8px; border-radius: 12px; font-size: 0.75em; font-weight: bold; text-transform: uppercase;">
                 {{ post.categories | first }}
               </span>
            </div>
          </div>
        </a>
      </div>
    {% endfor %}
  </div>
</section>

<script>
function filterArticles() {
  let input = document.getElementById('articleSearch').value.toLowerCase();
  let items = document.getElementsByClassName('article-item');
  
  for (let i = 0; i < items.length; i++) {
    let title = items[i].getAttribute('data-title');
    let categories = items[i].getAttribute('data-categories');
    
    if (title.includes(input) || categories.includes(input)) {
      items[i].classList.remove('hidden');
    } else {
      items[i].classList.add('hidden');
    }
  }
}
</script>

<section style="margin-top: 40px; padding: 25px; background-color: #f6f8fa; border-radius: 8px; border: 1px solid #e1e4e8;">
  <h2 style="margin-top: 0;">About the Project</h2>
  <p style="line-height: 1.6;">
    This platform is a dedicated space for transparent, data-driven economic analysis.
  </p>
  <p style="margin-top: 20px;"><strong>Contact:</strong> <a href="mailto:alisyedshujaat34@gmail.com" style="color: #0366d6; text-decoration: none; font-weight: bold;">alisyedshujaat34@gmail.com</a></p>
</section>

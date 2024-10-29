---
layout: page
title: Γεωλογικά Μνημεία
permalink: /pois/

---
<div class="pois-container">
  {% for p in site.data.pois %}
    <div class="poi-box">
      <a href="{{ p.url | relative_url }}">
        <img src="{{ '/assets/images/' | relative_url }}{{ p.image }}" alt="{{ p.title }}"/>
      </a>
      <h3>{{ p.title }}</h3>
      <p>{{ p.description }}</p>
    </div>
  {% endfor %}
</div>

<style>
.pois-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  padding: 20px;
}

.poi-box {
  width: 250px;
  margin: 20px;
  text-align: center;
}

.poi-box img {
  width: 100%;
  height: auto;
  border-radius: 8px;
}

.poi-box h3 {
  font-size: 18px;
  margin-top: 10px;
}

.poi-box p {
  font-size: 14px;
  color: #666;
}
</style>

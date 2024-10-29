---
layout: page
title: Γεωλογικά Μνημεία
permalink: /pois/

---
<div class="pois-container">
  {% for p in site.pois %}
    <div class="poi-box">
      <a href="{{ p.url | relative_url }}">
        <img src="/heritage-promotion/{{ p.image }}"/>
      </a>
      <h3>{{ p.title }}</h3>
        <p>{{ p.description }}</p>
    </div>
  {% endfor %}
</div>
<style>
.geological-monuments-container {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 24px;
  padding: 40px;
  background-color: #f0f4f8;
}

.geological-monument-card {
  background: linear-gradient(135deg, #a0d2eb, #00c6ff);
  border-radius: 16px;
  overflow: hidden;
  box-shadow: 0 6px 15px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease;
}

.geological-monument-card:hover {
  transform: scale(1.05);
}

.geological-monument-card img {
  width: 100%;
  height: 200px;
  object-fit: cover;
  border-bottom: 3px solid #fff;
}

.card-content {
  padding: 20px;
  color: #ffffff;
  text-align: center;
}

.card-content h3 {
  font-size: 22px;
  margin: 0 0 10px;
}

.card-content p {
  font-size: 14px;
  line-height: 1.6;
}
</style>

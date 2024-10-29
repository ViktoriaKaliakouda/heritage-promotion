---
layout: page
title: Γεωλογικά Μνημεία
permalink: /pois/

---
<div class="geological-monuments-container">
  <a href="URL_ΜΝΗΜΕΙΟΥ_1" class="geological-monument-card">
    <img src="assets/images/Lake_cave_σπηλαιο_λιμνων.JPG" alt="Σπήλαιο Λιμνών">
    <div class="card-content">
      <h3>Σπήλαιο Λιμνών</h3>
      <p>Μια σύντομη περιγραφή του μνημείου. Μπορείς να προσθέσεις περισσότερες λεπτομέρειες για να τραβήξεις το ενδιαφέρον του επισκέπτη.</p>
    </div>
  </a>
  <a href="URL_ΜΝΗΜΕΙΟΥ_2" class="geological-monument-card">
    <img src="URL_ΕΙΚΟΝΑΣ_2" alt="Όνομα Μνημείου 2">
    <div class="card-content">
      <h3>Όνομα Μνημείου 2</h3>
      <p>Περιγραφή για το μνημείο, με έναν πιο απαλό και διακριτικό τρόπο.</p>
    </div>
  </a>
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

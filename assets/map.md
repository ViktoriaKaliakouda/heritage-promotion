---
layout: page
title: Χάρτης
permalink: /map/
body_class: map-page
---
# Εξερεύνησε τα μνημεία στο χάρτη!
<html lang="el">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Διαδραστικός Χάρτης</title>
    <link rel="stylesheet" href="https://unpkg.com/leaflet/dist/leaflet.css" />
    <style>
        #map {
            height: 600px; /* Ύψος του χάρτη */
            width: 100%; /* Πλάτος του χάρτη */
        }
    </style>
</head>
<body>

<div id="map"></div>

<script src="https://unpkg.com/leaflet/dist/leaflet.js"></script>
<script>
    // Δημιουργία χάρτη
    var map = L.map('map').setView([38.0, 23.0], 6); // Ρύθμιση για Ελλάδα

    // Προσθήκη βασικού στρώματος χάρτη
    L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
        maxZoom: 19,
        attribution: '© OpenStreetMap'
    }).addTo(map);

    // Ορισμός των σημείων
    var points = [
        { coords: [39.2054, 25.9006], name: "Απολιθωμένο Δάσος Λέσβου" },
        { coords: [39.9941, 20.7866], name: "Δρακολίμνη Τύμφης" },
        { coords: [36.4035, 25.3942], name: "Καλντέρα Σαντορίνης" },
        { coords: [39.2568, 20.8438], name: "Κοκκινοπηλός Πρέβεζας" },
        { coords: [39.9738, 20.7256], name: "Κολυμπήθρες Πάπιγκο" },
        { coords: [38.0765, 22.2326], name: "Λίμνη Τσιβλού" },
        { coords: [38.2570, 20.6240], name: "Λιμνοσπήλαιο Μελισσάνης" },
        { coords: [39.7165, 21.6413], name: "Μετέωρα" },
        { coords: [37.9597, 22.1398], name: "Σπήλαιο Καστριών (Λιμνών)" },
        { coords: [35.2485, 23.9678], name: "Φαράγγι Σαμαριάς" }
    ];

    // Προσθήκη σημεία στο χάρτη
    points.forEach(function(point) {
        L.marker(point.coords).addTo(map)
            .bindPopup("<b>" + point.name + "</b>"); // Στην popup εμφανίζεται το όνομα του σημείου
    });
</script>

</body>
</html>

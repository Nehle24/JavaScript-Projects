# JavaScript-Projects
A collection of JavaScript assignments and coding projects from my web development course.
# JavaScript Projects

Welcome to my JavaScript Projects repository!

This repository contains all of my JavaScript assignments, challenges, and projects completed throughout this course. Each folder or file represents an exercise designed to strengthen my understanding of core JavaScript concepts and coding best practices.

## 📘 Contents
- Basic JavaScript exercises
- Functions and conditionals
- Loops and arrays
- DOM manipulation
- Event handling
- Final course project

## 💡 Purpose
This repository serves as both a learning record and part of my online coding portfolio. I will continue to update it as I progress through new lessons and challenges.

---
 Nehle24  
 JavaScript-Projects
OnePageWebsite/
│
├── index.html        ← your main web page
├── style.css         ← your CSS file for styling
├── script.js         ← your JavaScript file (for lightbox)
└── images/           ← a folder that holds your pictures
    ├── photo1.jpg
    ├── photo2.jpg
    ├── photo3.jpg
<h2>My Image Gallery</h2>
<div class="gallery">
  <img src="images/photo1.jpg" class="lightbox-img" alt="Photo 1">
  <img src="images/photo2.jpg" class="lightbox-img" alt="Photo 2">
  <img src="images/photo3.jpg" class="lightbox-img" alt="Photo 3">
</div>

<!-- Lightbox Modal -->
<div id="lightbox" class="lightbox">
  <img id="lightbox-img" src="">
</div>

<script src="script.js"></script>
<h2>My Image Gallery</h2>
<div class="gallery">
  <img src="images/photo1.jpg" class="lightbox-img" alt="Photo 1">
  <img src="images/photo2.jpg" class="lightbox-img" alt="Photo 2">
  <img src="images/photo3.jpg" class="lightbox-img" alt="Photo 3">
</div>

<!-- Lightbox Modal -->
<div id="lightbox" class="lightbox">
  <img id="lightbox-img" src="">
</div>

<script src="script.js"></script>
<h2>My Image Gallery</h2>
<div class="gallery">
  <img src="images/photo1.jpg" class="lightbox-img" alt="Photo 1">
  <img src="images/photo2.jpg" class="lightbox-img" alt="Photo 2">
  <img src="images/photo3.jpg" class="lightbox-img" alt="Photo 3">
</div>

<!-- Lightbox Modal -->
<div id="lightbox" class="lightbox">
  <img id="lightbox-img" src="">
</div>

<script src="script.js"></script>

body {
  font-family: Arial, sans-serif;
  text-align: center;
  background-color: #f5f5f5;
}

.gallery {
  display: flex;
  justify-content: center;
  gap: 15px;
  flex-wrap: wrap;
  margin-top: 20px;
}

.gallery img {
  width: 200px;
  height: 150px;
  object-fit: cover;
  border-radius: 10px;
  cursor: pointer;
  transition: transform 0.3s ease;
}

.gallery img:hover {
  transform: scale(1.1);
}

.lightbox {
  display: none;
  position: fixed;
  z-index: 1000;
  top: 0; left: 0;
  width: 100%; height: 100%;
  background: rgba(0, 0, 0, 0.8);
  justify-content: center;
  align-items: center;
}

.lightbox img {
  max-width: 80%;
  max-height: 80%;
  border-radius: 10px;
}
const lightbox = document.getElementById('lightbox');
const lightboxImg = document.getElementById('lightbox-img');

document.querySelectorAll('.lightbox-img').forEach(img => {
  img.addEventListener('click', () => {
    lightbox.style.display = 'flex';
    lightboxImg.src = img.src;
  });
});

lightbox.addEventListener('click', () => {
  lightbox.style.display = 'none';
});

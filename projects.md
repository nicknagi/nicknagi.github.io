---
layout: default
title: Projects
---

<div class="filter-header">
  <div class="filter-label">Filter Projects:</div>
  <div class="filter-buttons">
    <button class="filter-btn active" data-filter="all">All</button>
    <button class="filter-btn" data-filter="ml">Machine Learning</button>
    <button class="filter-btn" data-filter="systems">Systems & Distributed</button>
    <button class="filter-btn" data-filter="research">Research</button>
  </div>
</div>

<div class="projects-grid">

  <div class="project-card show" data-tags="ml python research">
    <div class="project-card-header">
      <h3 class="project-title">Federated Learning For WIFI Fingerprinting</h3>
      <span class="project-date">2022</span>
    </div>
    {% include technologies.html technologies="git python" %}
    <p class="project-description">
      Research project involving applying state-of-the-art ML learning methods to the field of wireless communications. Research was conducted at the University of Toronto WirLab lead by Prof. Shahrokh Valaee and under the guidance of a PhD student.
    </p>
    <p class="project-description">
      First author on a paper published at the International Conference on Communications 2022 in Seoul, South Korea.
    </p>
    <div class="project-links">
      <a href="https://ieeexplore.ieee.org/document/9838945" target="_blank" class="project-link-btn"><i class="fas fa-file-alt"></i> Paper Link</a>
    </div>
  </div>

  <div class="project-card show" data-tags="systems python aws digital-ocean">
    <div class="project-card-header">
      <h3 class="project-title">Assesing The Scalability Of SAWCAP Algorithm</h3>
      <span class="project-date">2021</span>
    </div>
    {% include technologies.html technologies="git python aws digital-ocean" %}
    <p class="project-description">
      Final year project completed in a team of 4 undergraduate students under the supervision of Professor Cristiana Amza.
    </p>
    <p class="project-description">
      Project involved assessing the scalability of the Semantic-Aware Resource Characterization and Prediction (SAWCAP) algorithm on a large-scale Hadoop cluster (&gt; 100 Virtual Machines).
    </p>
    <div class="project-links">
      <a href="http://sysweb.cs.toronto.edu/publication_files/0000/0360/CLOUD2020.pdf" target="_blank" class="project-link-btn"><i class="fas fa-file-alt"></i> Paper</a>
      <a href="https://github.com/nicknagi/SAWCAP-Scalability" target="_blank" class="project-link-btn"><i class="fab fa-github"></i> GitHub</a>
    </div>
  </div>

  <div class="project-card show" data-tags="systems rust">
    <div class="project-card-header">
      <h3 class="project-title">Physics Simulator</h3>
      <span class="project-date">2021</span>
    </div>
    {% include technologies.html technologies="git rust" %}
    <div class="project-video-wrapper">
      <video class="project-video" controls loop>
        <source src="https://user-images.githubusercontent.com/14340000/117508795-27d1ab80-af57-11eb-9566-2863e8106ed3.mov">
        Your browser does not support the video tag.
      </video>
    </div>
    <p class="project-description">
      A Newtonian physics simulator built in Rust. The main goal of the project was to learn the Rust programming language.
    </p>
    <p class="project-description">
      Particles are modelled as circles in 2D space. Collision detection is used to simulate elastic collisions.
    </p>
    <div class="project-links">
      <a href="https://github.com/nicknagi/rust-physics-simulation" target="_blank" class="project-link-btn"><i class="fab fa-github"></i> GitHub</a>
    </div>
  </div>

  <div class="project-card show" data-tags="ml python">
    <div class="project-card-header">
      <h3 class="project-title">Executing Assembly With Deep Learning</h3>
      <span class="project-date">2021</span>
    </div>
    {% include technologies.html technologies="git python" %}
    <p class="project-description">
      A sequence-to-sequence LSTM model to run a sequence of assembly instructions and output the final register states. More can be found in the project's GitHub repository.
    </p>
    <div class="project-links">
      <a href="https://github.com/nicknagi/assembly-execution-rnn" target="_blank" class="project-link-btn"><i class="fab fa-github"></i> GitHub</a>
    </div>
  </div>

  <div class="project-card show" data-tags="systems java">
    <div class="project-card-header">
      <h3 class="project-title">Distributed Key-Value Store</h3>
      <span class="project-date">2021</span>
    </div>
    {% include technologies.html technologies="git java" %}
    <p class="project-description">
      Project done as part of Winter 2021 ECE419 Distributed Systems course.
    </p>
    <p class="project-description">
      A distributed key-value store implemented from scratch in Java. The database uses consistent hashing to distribute keys among the nodes in the cluster. Replication is used to achieve fault-tolerance.
    </p>
  </div>

  <div class="project-card show" data-tags="ml python">
    <div class="project-card-header">
      <h3 class="project-title">Course Project: Waste Classification</h3>
      <span class="project-date">2021</span>
    </div>
    {% include technologies.html technologies="git python" %}
    <p class="project-description">
      Project done as part of Winter 2021 APS360 Artificial Intelligence Fundamentals course.
    </p>
    <p class="project-description">
      A CNN model to categorize waste as organic or recyclable.
    </p>
    <div class="project-links">
      <a href="https://github.com/nicknagi/APS360" target="_blank" class="project-link-btn"><i class="fab fa-github"></i> GitHub</a>
    </div>
  </div>

</div>

<script>
document.addEventListener("DOMContentLoaded", function() {
  const buttons = document.querySelectorAll(".filter-btn");
  const cards = document.querySelectorAll(".project-card");

  buttons.forEach(btn => {
    btn.addEventListener("click", () => {
      buttons.forEach(b => b.classList.remove("active"));
      btn.classList.add("active");

      const filterValue = btn.getAttribute("data-filter");

      cards.forEach(card => {
        const tags = card.getAttribute("data-tags").split(" ");
        if (filterValue === "all" || tags.includes(filterValue)) {
          card.style.display = "flex";
          setTimeout(() => {
            card.classList.add("show");
          }, 50);
        } else {
          card.classList.remove("show");
          setTimeout(() => {
            card.style.display = "none";
          }, 300);
        }
      });
    });
  });
});
</script>
<script lang="ts">
    let currentIndex = 0;
    let slides: NodeListOf<HTMLElement>;
    let totalSlides = 0;
  
    if (typeof window !== "undefined") {
      slides = document.querySelectorAll(".slide");
      totalSlides = slides.length;
  
      function updateSlide(index: number) {
        slides.forEach((slide, i) => {
          slide.classList.remove("active");
          slide.style.transform = `translateX(${100 * (i - index)}%)`;
        });
        slides.item(index)?.classList.add("active");
      }
  
      function nextSlide() {
        currentIndex = (currentIndex + 1) % totalSlides;
        updateSlide(currentIndex);
      }
  
      function prevSlide() {
        currentIndex = (currentIndex - 1 + totalSlides) % totalSlides;
        updateSlide(currentIndex);
      }
  
      document.getElementById("next")?.addEventListener("click", nextSlide);
      document.getElementById("prev")?.addEventListener("click", prevSlide);
  
      updateSlide(currentIndex);
    }
  </script>
  
  <div id="slider-container">
    <div id="slider">
      <div class="slide active">
        <img src="https://static.wikia.nocookie.net/minecraft_gamepedia/images/f/ff/Polished_Andesite_(texture)_JE2_BE2.png" alt="" />
        <div class="text-content">
          <h2>Nazwa 1</h2>
          <p>Opis 1</p>
        </div>
      </div>
      <div class="slide">
        <img
          src="https://static.wikia.nocookie.net/minecraft_gamepedia/images/8/82/Polished_Granite_(texture)_JE2_BE2.png"
          alt=""
        />
        <div class="text-content">
          <h2>Nazwa 2</h2>
          <p>Opis 2</p>
        </div>
      </div>
      <div class="slide">
        <img src="https://static.wikia.nocookie.net/minecraft_gamepedia/images/d/de/Polished_Diorite_(texture)_JE2_BE2.png" alt="" />
        <div class="text-content">
          <h2>Nazwa 3</h2>
          <p>Opis 3</p>
        </div>
      </div>
    </div>
    <button id="prev">&#10094;</button>
    <button id="next">&#10095;</button>
  </div>
  
  <style>
    #slider-container {
      position: relative;
      width: 100%;
      height: 800px;
      margin: auto;
      overflow: hidden;
      background-image: url("https://static.wikia.nocookie.net/minecraft_gamepedia/images/7/71/Deepslate_Tiles_(texture)_JE2.png");
    }
  
    #slider {
      display: flex;
      transition: transform 0.5s ease-in-out;
      height: 100%;
      align-items: center;
    }
  
    .slide {
      min-width: 100%;
      text-align: center;
      position: absolute;
      transition: transform 0.5s ease-in-out;
      display: none;
      display: flex;
      flex-wrap: wrap; /* Umożliwia zawijanie elementów */
      align-items: center; /* Wyśrodkowanie w pionie */
      justify-content: space-evenly; /* Wyśrodkowanie w poziomie */
    }
  
    .slide img {
      max-width: 50%; /* Obraz zajmuje maksymalnie 50% szerokości */
      height: auto;
    }
  
    .text-content {
      max-width: 50%; /* Tekst zajmuje maksymalnie 50% szerokości */
      text-align: left;
      padding: 20px;
      font-size: 3rem;
      font-family: var(--minecraft-font);
    }
  
    .slide.active {
      display: flex;
    }
  
    button {
      position: absolute;
      top: 50%;
      transform: translateY(-50%);
      background: rgba(0, 0, 0, 0.5);
      color: white;
      border: none;
      cursor: pointer;
      padding: 10px;
    }
  
    #prev {
      left: 0;
    }
  
    #next {
      right: 0;
    }
  
    /* Zapytanie medialne dla węższych ekranów */
    @media (max-width: 768px) {
      .slide {
        flex-direction: column; /* Układ pionowy na węższych ekranach */
        text-align: center;
      }
  
      .slide img,
      .text-content {
        max-width: 100%; /* Obraz i tekst zajmują 100% szerokości */
      }
  
      .text-content {
        text-align: center;
      }
    }
  </style>
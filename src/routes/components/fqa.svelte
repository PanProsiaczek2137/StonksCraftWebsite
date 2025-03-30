<script>
    let faqs = [
      { question: "Opis", answer: "  Lorem ipsum dolor sit amet consectetur, adipisicing elit. Sequi, vel molestias neque corrupti aliquid porro vitae nemo exercitationem corporis incidunt. Eum iusto recusandae alias et quaerat aspernatur quia, illum molestiae!" },
      { question: "Opis", answer: "odpowiedź" },
      { question: "Opis", answer: "odpowiedź" },
      { question: "Opis", answer: "odpowiedź" },
      { question: "Opis", answer: "odpowiedź" },
      { question: "Opis", answer: "odpowiedź" },
      { question: "Opis", answer: "odpowiedź" },
      { question: "Opis", answer: "odpowiedź" },
      { question: "Opis", answer: "odpowiedź" },
      { question: "Opis", answer: "odpowiedź" },
      { question: "Opis", answer: "odpowiedź" },
      { question: "Opis", answer: "odpowiedź" },
      { question: "Opis", answer: "odpowiedź" },
      { question: "Opis", answer: "odpowiedź" },
      { question: "Opis", answer: "odpowiedź" },
      { question: "Opis", answer: "odpowiedź" },
      { question: "Opis", answer: "odpowiedź" },
      { question: "Opis", answer: "odpowiedź" },
      { question: "Opis", answer: "odpowiedź" },
      { question: "Opis", answer: "odpowiedź" },
    ];
  </script>
  
  <style>
    .faq-section {
      display: flex;
      flex-wrap: wrap;
      height: 800px;
      width: 100%;
      gap: 20px;
      padding: 20px;
      box-sizing: border-box;
      justify-content: center;
      overflow-y: auto;
      background-image: url("https://static.wikia.nocookie.net/minecraft_gamepedia/images/3/3e/Mushroom_Block_(inside_texture)_JE2_BE2.png");
    }
  
    .faq-card {
      background-image: url("https://static.wikia.nocookie.net/minecraft_gamepedia/images/8/8b/White_Wool_(texture)_JE2_BE2.png");
      background-size: 130px;
      flex: 1 1 300px;
      min-width: 250px;
      max-width: 350px;
      border: 1px solid #ddd;
      border-radius: 8px;
      padding: 20px;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
    }
  
    .faq-card h3 {
      margin: 0;
      font-size: 2rem;
      font-weight: bold;
      font-family: var(--minecraft-font);
    }
  
    .faq-card p {
      font-size: 1rem;
      margin-top: 10px;
      line-height: 1.5;
    }
  </style>
  
  <div class="faq-section">
    {#each faqs as { question, answer }}
      <div class="faq-card">
        <h3>{question}</h3>
        <p>{answer}</p>
      </div>
    {/each}
  </div>
  
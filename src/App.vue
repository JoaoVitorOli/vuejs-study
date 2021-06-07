<template>
  <div id="app">
    <div class="Container">
      <div class="Box Sedans">
        <img src="./assets/icon-sedans.svg" class="image" alt="icon">
        <h1 class="head">SEDANS</h1>
        <p class="paragraph">
          Choose a sedan for its affordability and excellent fuel economy. Ideal for cruising in the city 
          or on your next road trip.
        </p>
        <Button value="Learn More" color="Sedans" />
      </div>
      <div class="Box Suvs">
        <img src="./assets/icon-suvs.svg" class="image" alt="icon">
        <h1 class="head">SUVs</h1>
        <p class="paragraph">
          Take an SUV for its spacious interior, power, and versatility. Perfect for your next family vacation 
          and off-road adventures.
        </p>
        <Button value="Learn More" color="Suvs" />
      </div>
      <div class="Box Luxury">
        <img src="./assets/icon-luxury.svg" class="image" alt="icon">
        <h1 class="head">LUXURY</h1>
        <p class="paragraph">
          Cruise in the best car brands without the bloated prices. Enjoy the enhanced comfort of a luxury 
          rental and arrive in style.
        </p>
        <Button value="Learn More" color="Luxury" />
      </div>
    </div>
  </div>
</template>

<script>
  import Button from "./components/Button.vue";

  export default {
    name: 'App',
    components: {
      Button
    }
  }
</script>

<style>
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }

  body {
    background: hsla(0, 0%, 100%, 0.75);
  }

  #app {
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .Container {
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);

    max-width: 900px;
    width: 100%;
    padding: 0 2rem;

    display: grid;
    grid-template-columns: 1fr 1fr 1fr;

    border-radius: 8px;
  }

  .Box {
    padding: 3rem;
  }

  .Box.Sedans {
    background: hsl(31, 77%, 52%);
    border-radius: 8px 0 0 8px;
  }

  .Box.Suvs {
    background: hsl(184, 100%, 22%);
  }

  .Box.Luxury {
    background: hsl(179, 100%, 13%);
    border-radius: 0 8px 8px 0;
  }

  .image, .head {
    margin-bottom: 2rem;
  }

  .paragraph {
    color: hsla(0, 0%, 100%, 0.75);
    font-family: "Lexend Deca", sans-serif;
    font-size: 15px;
    line-height: 1.5rem;
    margin-bottom: 4rem;
  }

  .head {
    color: hsl(0, 0%, 95%);
    font-family: "Big Shoulders Display", sans-serif;
    font-size: 2.75rem;
  }

  @media (max-width: 768px) {
    .Container {
      position: relative;
      left: 0;
      top: 0;
      transform: none;
      padding: 5.75rem 2rem;

      grid-template-columns: 1fr;
    }

    .Box.Sedans {
      border-radius: 8px 8px 0 0;
    }

    .Box.Luxury {
      border-radius: 0 0 8px 8px;
    }

    .paragraph {
      font-size: 14px;
    }
  }

  @media (max-width: 425px) {
    .Box {
      padding: 2rem;
    }

    .head {
      font-size: 2.5rem;
    }

    .paragraph {
      font-size: 12px;
      margin-bottom: 2rem;
    }
  }
</style>

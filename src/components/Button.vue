<template lang="pt-br">
  <button id="Button" v-bind:class="this.color">
    {{value}}
  </button>
</template>

<script>
  export default {
    name: "Button",
    props: {
      value: String,
      color: String
    }
  }
</script>

<style scoped>
  #Button {
    padding: 1rem 2rem;
    margin-top: auto;

    border: 2px solid hsl(0, 0%, 95%);
    background: hsl(0, 0%, 95%);
    outline: none;
    border-radius: 50px;

    font-family: "Lexend Deca", sans-serif;
    font-size: 1rem;

    cursor: pointer;
    transition: 0.2s;
  }

  #Button:hover {
    background: transparent;
    color: hsl(0, 0%, 95%);
  }

  .Sedans {
    color: hsl(31, 77%, 52%);
  }

  .Suvs {
    color: hsl(184, 100%, 22%);
  }

  .Luxury {
    color: hsl(179, 100%, 13%);
  }

  @media (max-width: 824px) {
    #Button {
      font-size: 14px;
      padding: 0.75rem 1.75rem;
    }
  }
 </style>
<template>
    <section class="home" id="home">
      <div class="max-width">
        <div class="home-content">
          <div class="text-1">Helloooooo! I am</div>
          <div class="text-2">Jassim <span>Junaid</span></div>
          <div class="text-3"> FUTURE <span class="typing"></span></div>
          <p>I am a sassy and bold individual who confidently expresses myself and embraces risks.</p>
          <p>My sharp wit and self-assured demeanor leave a lasting impression on people.</p>
        </div>
      </div>
    </section>
  </template>
  
  <script>
  import Typed from 'typed.js';
  
  export default {
    mounted() {
      this.initTyped();
    },
    methods: {
      initTyped() {
        new Typed(".typing", {
          strings: ["PROGRAMMER!", "DEVELOPER!"],
          typeSpeed: 80,
          backSpeed: 40,
          loop: true
        });
      }
    }
  };
  </script>
  
  <style scoped>
  
  </style>
  
<template>
    <section class="about" id="about">
      <div class="max-width">
        <h2 class="title">About me</h2>
        <div class="about-content">
          <div class="column left">
            <img src="@/assets/about.jpg" alt="About Me">
          </div>
          <div class="column right">
            <div class="text"> NONCHALANT <span class="typing-2"></span></div>
            <p>Hello, my name is Jassim Disamburun Junaid, and I am 23 years old. I am from Marawi City, but grew up in Manila. 
                I am an undergrad student taking up Bachelor of Science in Computer Science, and I hope to become a Programmer and to be part in IT industry in the future. 
                During my free time, I enjoy listening music and watching movies or series. I also love exploring and travelling to new places.  
                As a person, I am an ambivert, which means that my personality type is equally fulfilled whether I'm out in a crowd or at home doing something alone and depends on the person I am with. 
                I'm also interested in sports specifically Basketball.</p>
          </div>
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
        new Typed(".typing-2", {
          strings: ["DAW KUNO!"],
          typeSpeed: 100,
          backSpeed: 60,
          loop: true
        });
      }
    }
  };
  </script>
  
  <style scoped>
  
  </style>
  
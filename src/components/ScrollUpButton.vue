<template>
    <div class="scroll-up-btn" v-if="isVisible" @click="scrollToTop">
      <i class="fas fa-angle-up"></i>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        isVisible: false
      };
    },
    mounted() {
      window.addEventListener('scroll', this.handleScroll);
    },
    unmounted() {
      window.removeEventListener('scroll', this.handleScroll);
    },
    methods: {
      handleScroll() {
        if (window.scrollY > 500) {
          this.isVisible = true;
        } else {
          this.isVisible = false;
        }
      },
      scrollToTop() {
        window.scrollTo({
          top: 0,
          behavior: 'smooth'
        });
      }
    }
  };
  </script>
  
  
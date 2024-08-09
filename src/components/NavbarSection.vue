<template>
    <div>
      <!-- Scroll-up Button -->
      <div class="scroll-up-btn" :class="{ 'show': isScrollUpVisible }">
        <i class="fas fa-angle-up" @click="scrollToTop"></i>
      </div>
  
      <!-- Navbar -->
      <nav class="navbar" :class="{ 'sticky': isNavbarSticky }">
        <div class="max-width">
          <div class="logo"><a href="#">My Port<span>folio.</span></a></div>
          <ul class="menu">
            <li><a href="#home" @click.prevent="scrollToSection('#home')">Home</a></li>
            <li><a href="#about" @click.prevent="scrollToSection('#about')">About</a></li>
            <li><a href="#education" @click.prevent="scrollToSection('#education')">Education</a></li>
            <li><a href="#skills" @click.prevent="scrollToSection('#skills')">Skills</a></li>
            <li><a href="#hobbies" @click.prevent="scrollToSection('#hobbies')">Hobbies</a></li>
            <li><a href="#future" @click.prevent="scrollToSection('#future')">Future Plan</a></li>
          </ul>
          <div class="menu-btn" @click="toggleMenu">
            <i class="fas fa-bars"></i>
          </div>
        </div>
      </nav>
    </div>
  </template>
  
  <script>
  import $ from 'jquery';
  
  export default {
    data() {
      return {
        isNavbarSticky: false,
        isScrollUpVisible: false
      };
    },
    mounted() {
      // Initialize scroll listeners
      $(window).scroll(() => {
        this.isNavbarSticky = window.scrollY > 20;
        this.isScrollUpVisible = window.scrollY > 500;
      });
  
      // Smooth scroll on menu items click
      $('.navbar .menu li a').click((event) => {
        const target = $(event.currentTarget).attr('href');
        this.scrollToSection(target);
      });
    },
    methods: {
      // Scroll to top function
      scrollToTop() {
        $('html, body').animate({ scrollTop: 0 }, 800);
      },
  
      // Toggle menu/navbar script
      toggleMenu() {
        $('.navbar .menu').toggleClass('active');
        $('.menu-btn i').toggleClass('active');
      },
  
      // Scroll to section on menu item click
      scrollToSection(target) {
        const offset = $(target).offset().top;
        $('html, body').animate({ scrollTop: offset }, 800);
      }
    }
  };
  </script>
  
  <style scoped>
  /* Scoped styles for Navbar.vue */
  </style>
  
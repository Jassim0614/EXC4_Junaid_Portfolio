<template>
    <section class="hobbies" id="hobbies">
        <div class="max-width">
            <h2 class="title">My Hobbies</h2>
            <div class="carousel owl-carousel">
                <div class="card">
                    <div class="box">
                        <img src="@\assets\playinggames.jpg" alt="">
                        <div class="text">Playing Games</div>
                        <p> I derive immense pleasure from gaming, whether it's on mobile or computer. I enjoy exploring virtual worlds, and participating in competitive gameplay.</p>
                    </div>
                </div>
                <div class="card">
                    <div class="box">
                        <img src="@\assets\playingbasketball.jpg" alt="">
                        <div class="text">Playing Basketball</div>
                        <p>This brings me joy, fitness, and a competitive spirit as I engage in a fast-paced sport that challenges my agility, coordination, and strategic thinking.</p>
                    </div>
                </div>
                <div class="card">
                    <div class="box">
                        <img src="@\assets\travelling.jpg" alt="">
                        <div class="text">Travelling</div>
                        <p>It fuels my adventurous spirit, and provides me with unforgettable experiences as I explore diverse cultures and stunning destinations around the world.</p>
                    </div>
                </div>
                <div class="card">
                    <div class="box">
                        <img src="@\assets\listeningmusic.jpg" alt="">
                        <div class="text">Listening Music</div>
                        <p>This brings me pure joy, creative expression, and a sense of freedom as I move to the rhythm, embody emotions, and connect with the music.</p>
                    </div>
                </div>
                <div class="card">
                    <div class="box">
                        <img src="@\assets\catcompanion.jpg" alt="">
                        <div class="text">Cat Companion</div>
                        <p> The name of my cat is Teddy, skl. I enjoy spending time with him and I consider my cat a stress reliever. He is very sweet, especially when I have food.</p>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>


<script>

import $ from 'jquery'; // Import jQuery
/* import 'owl.carousel'; */

export default {
  mounted() {
    this.initCarousel();
  },
  methods: {
    initCarousel() {
      this.$nextTick(() => {
        $('.carousel').owlCarousel({
          margin: 20,
          loop: true,
          autoplay: true,
          autoplayTimeout: 2000,
          autoplayHoverPause: true,
          responsive: {
            0: {
              items: 1,
              nav: false
            },
            600: {
              items: 2,
              nav: false
            },
            1000: {
              items: 3,
              nav: false
            }
          }
        });
      });
    }
  }
};
</script>


<style scoped>
/* Scoped styles */
</style>

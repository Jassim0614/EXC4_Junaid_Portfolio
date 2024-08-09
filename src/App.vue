<template>
  <div>
    <div class="scroll-up-btn">
      <i class="fas fa-angle-up"></i>
    </div>

    <ScrollUpButton />
    <NavbarSection />
    <HomeSection />
    <AboutSection />
    <EducationSection />
    <SkillsSection />
    <HobbiesSection />
    <FutureSection />
    <footer>
      <p>Jassim Junaid</p>
      <p>For more details - please click on the square below:</p>
    </footer>
  </div>
</template>

<script>
import ScrollUpButton from './components/ScrollUpButton.vue'
import NavbarSection from './components/NavbarSection.vue'
import HomeSection from './components/HomeSection.vue'
import AboutSection from './components/AboutSection.vue'
import EducationSection from './components/EducationSection.vue'
import SkillsSection from './components/SkillsSection.vue'
import HobbiesSection from './components/HobbiesSection.vue'
import FutureSection from './components/FutureSection.vue'


export default {
  name: 'App',
  components: {
    ScrollUpButton,
    NavbarSection,
    HomeSection,
    AboutSection,
    EducationSection,
    SkillsSection,
    HobbiesSection,
    FutureSection,
    
  }
}
</script>


<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&family=Ubuntu:wght@400;500;700&display=swap');
@import 'https://cdnjs.cloudflare.com/ajax/libs/font-awesome/5.15.3/css/all.min.css';
/* @import 'owl.carousel/dist/assets/owl.carousel.min.css';
@import 'owl.carousel/dist/assets/owl.theme.default.min.css'; */

*{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    text-decoration: none;
}
html{
    scroll-behavior: smooth;
}

/* custom scroll bar */
::-webkit-scrollbar {
    width: 10px;
}
::-webkit-scrollbar-track {
    background: #f1f1f1;
}
::-webkit-scrollbar-thumb {
    background: #888;
}

::-webkit-scrollbar-thumb:hover {
    background: #555;
}

section{
    padding: 100px 0;
}
.max-width{
    max-width: 1300px;
    padding: 0 80px;
    margin: auto;
}
.about, .education, .skills, .hobbies, .future, footer{
    font-family: 'Poppins', sans-serif;
}
.about .about-content,
.education .edu-content,
.skills .skills-content,
.future .fp-content{
    display: flex;
    align-items: center;
    justify-content: space-between;
}
section .title{
    position: relative;
    text-align: center;
    font-size: 40px;
    font-weight: 500;
    margin-bottom: 60px;
    padding-bottom: 20px;
    font-family: 'Ubuntu', sans-serif;
}
section .title::before{
    content: "";
    position: absolute;
    bottom: 0px;
    left: 50%;
    width: 180px;
    height: 3px;
    background: #111;
    transform: translateX(-50%);
}
section .title::after{
    position: absolute;
    bottom: -8px;
    left: 50%;
    font-size: 20px;
    color: crimson;
    padding: 0 5px;
    background: #fff;
    transform: translateX(-50%);
}

/* navbar */
.navbar{
    position: fixed;
    width: 100%;
    z-index: 999;
    padding: 30px 0;
    font-family: 'Ubuntu', sans-serif;
    transition: all 0.3s ease;
}
.navbar.sticky{
    padding: 15px 0;
    background: crimson;
}
.navbar .max-width{
    display: flex;
    align-items: center;
    justify-content: space-between;
}
.navbar .logo a{
    color: #fff;
    font-size: 35px;
    font-weight: 600;
}
.navbar .logo a span{
    color: crimson;
    transition: all 0.3s ease;
}
.navbar.sticky .logo a span{
    color: #fff;
}
.navbar .menu li{
    list-style: none;
    display: inline-block;
}
.navbar .menu li a{
    display: block;
    color: #fff;
    font-size: 18px;
    font-weight: 500;
    margin-left: 25px;
    transition: color 0.3s ease;
}
.navbar .menu li a:hover{
    color: crimson;
}
.navbar.sticky .menu li a:hover{
    color: #fff;
}

/* menu btn */
.menu-btn{
    color: #fff;
    font-size: 23px;
    cursor: pointer;
    display: none;
}
.scroll-up-btn{
    position: fixed;
    height: 45px;
    width: 42px;
    background: crimson;
    right: 30px;
    bottom: 10px;
    text-align: center;
    line-height: 45px;
    color: #fff;
    z-index: 9999;
    font-size: 30px;
    border-radius: 6px;
    border-bottom-width: 2px;
    cursor: pointer;
    opacity: 0;
    pointer-events: none;
    transition: all 0.3s ease;
}
.scroll-up-btn.show{
    bottom: 30px;
    opacity: 1;
    pointer-events: auto;
}
.scroll-up-btn:hover{
    filter: brightness(90%);
}


/* home section */
.home{
    display: flex;
    background: url("C:\Users\Jassim Junaid\converison_portfolio\src\assets\meme.jpg") no-repeat center;
    height: 100vh;
    color: #fff;
    min-height: 500px;
    background-size: cover;
    background-attachment: fixed;
    font-family: 'Ubuntu', sans-serif;
}
.home .max-width{
  width: 100%;
  display: flex;
}
.home .max-width .row{
  margin-right: 0;
}
.home .home-content .text-1{
    font-size: 27px;
}
.home .home-content .text-2{
    font-size: 85px;
    font-weight: 600;
    margin-left: -3px;
}
.home .home-content .text-3{
    font-size: 50px;
    margin: 5px 0;
}
.home .home-content a{
    display: inline-block;
    background: crimson;
    color: #fff;
    font-size: 25px;
    padding: 12px 36px;
    margin-top: 20px;
    font-weight: 400;
    border-radius: 6px;
    border: 2px solid crimson;
    transition: all 0.3s ease;
}
.home .home-content a:hover{
    color: crimson;
    background: none;
}
span{
    color: crimson;
}

/* about section */
.about .title::after{
    content: "who i am";
}
.about .about-content .left img{
    height: 400px;
    width: 450px;
    object-fit: cover;
    border-radius: 6px;
}
.about .about-content .right{
    width: 55%;
}
.about .about-content .right .text{
    font-size: 30px;
    font-weight: bold;
    margin-bottom: 10px;
}
.about .about-content .right .text span{
    color: crimson;
}

/* education section */
.education, .hobbies{
    color:#fff;
    background: #111;
}
.education .title::before,
.hobbies .title::before{
    background: #fff;
}
.education .title::after,
.hobbies .title::after{
    background: #111;
    content: "where i studied";
}
.education .edu-content .card{
    width: calc(33% - 20px);
    background: #222;
    text-align: center;
    border-radius: 6px;
    padding: 50px 50px;
    cursor: pointer;
    transition: all 0.3s ease;
}
.education .edu-content .card:hover{
    background: crimson;
}
.education .edu-content .card .box{
    transition: all 0.3s ease;
}
.education .edu-content .card:hover .box{
    transform: scale(1.05);
}
.education .edu-content .card i{
    font-size: 50px;
    color: crimson;
    transition: color 0.3s ease;
}
.education .edu-content .card:hover i{
    color: #fff;
}
.education .edu-content .card .text{
    font-size: 27px;
    font-weight: 500;
    margin: 10px 0 7px 0;
}

/* skills section */

.skills .title::after{
    content: "what i know";
}
.skills .skills-content .column{
    width: calc(50% - 30px);
}
.skills .skills-content .left .text{
    font-size: 30px;
    font-weight: 600;
    margin-bottom: 10px;
}
.skills .skills-content .left p{
    text-align: justify;
}
.skills .skills-content .left a{
    display: inline-block;
    background: crimson;
    color: #fff;
    font-size: 18px;
    font-weight: 500;
    padding: 8px 16px;
    margin-top: 20px;
    border-radius: 6px;
    border: 2px solid crimson;
    transition: all 0.3s ease;
}
.skills .skills-content .left a:hover{
    color: crimson;
    background: none;
}
.skills .skills-content .right .bars{
    margin-bottom: 15px;
}
.skills .skills-content .right .info{
    display: flex;
    margin-bottom: 5px;
    align-items: center;
    justify-content: space-between;
}
.skills .skills-content .right span{
    font-weight: 500;
    font-size: 18px;
}
.skills .skills-content .right .line{
    height: 13px;
    width: 100%;
    background: lightgrey;
    position: relative;
}
.skills .skills-content .right .line::before{
    content: "";
    position: absolute;
    height: 100%;
    left: 0;
    top: 0;
    background: crimson;
}
.skills-content .right .mysql::before{
    width: 90%;
}
.skills-content .right .c::before{
    width: 60%;
}
.skills-content .right .photography::before{
    width: 80%;
}
.skills-content .right .communication::before{
    width: 50%;
}
.skills-content .right .ps::before{
    width: 70%;
}

/* hobbies section */
.hobbies .title::after{
    content: "hobbies for life";
}
.hobbies .carousel .card{
    background: #222;
    border-radius: 6px;
    padding: 25px 35px;
    text-align: center;
    overflow: hidden;
    transition: all 0.3s ease;
}
.hobbies .carousel .card:hover{
    background: crimson;
}
.hobbies .carousel .card .box{
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    transition: all 0.3s ease;
}
.hobbies .carousel .card:hover .box{
    transform: scale(1.05);
}
.hobbies .carousel .card .text{
    font-size: 25px;
    font-weight: 500;
    margin: 10px 0 7px 0;
}
.hobbies .carousel .card img{
    height: 200px;
    width: 200px;
    object-fit: cover;
    border-radius: 50%;
    border: 5px solid crimson;
    transition: all 0.3s ease;
}
.hobbies .carousel .card:hover img{
    border-color: #fff;
}
.owl-dots{
    text-align: center;
    margin-top: 20px;
}
.owl-dot{
    height: 13px;
    width: 13px;
    margin: 0 5px;
    outline: none!important;
    border-radius: 50%;
    border: 2px solid crimson!important;
    transition: all 0.3s ease;
}
.owl-dot.active{
    width: 35px;
    border-radius: 14px;
}
.owl-dot.active,
.owl-dot:hover{
    background: crimson!important;
}

/* future plan section */
.future .title::after{
    content: "what i want to";
}
.future .fp-content .column{
    width: calc(50% - 30px);
}
.future .fp-content .text{
    font-size: 30px;
    font-weight: 600;
    margin-bottom: 10px;
}
.future .fp-content .left p{
    text-align: justify;
}
.future .fp-content .left .icons{
    margin: 15px 0;
}
.future .fp-content .row{
    display: flex;
    height: 65px;
    align-items: center;
    
}
.future .fp-content .row .info{
    margin-left: 30px;

}
.future .fp-content .row i{
    font-size: 30px;
    color: crimson;
}
.future .fp-content .info .head{
    font-weight: bold;
}

.future .fp-content .right{
    width: 38%;
}
.future .fp-content .right img{
    height: 500px;
    width: 500px;
    object-fit: cover;
}

/* footer section */

footer{
    background: #111;
    padding: 15px 23px;
    color: #fff;
    text-align: center;
}

/* responsive media query start */
@media (max-width: 1104px) {
    .about .about-content .left img{
        height: 350px;
        width: 350px;
    }
}

@media (max-width: 991px) {
    .max-width{
        padding: 0 50px;
    }
}
@media (max-width: 947px){
    .menu-btn{
        display: block;
        z-index: 999;
    }
    .menu-btn i.active:before{
        content: "\f00d";
    }
    .navbar .menu{
        position: fixed;
        height: 100vh;
        width: 100%;
        left: -100%;
        top: 0;
        background: #111;
        text-align: center;
        padding-top: 80px;
        transition: all 0.3s ease;
    }
    .navbar .menu.active{
        left: 0;
    }
    .navbar .menu li{
        display: block;
    }
    .navbar .menu li a{
        display: inline-block;
        margin: 20px 0;
        font-size: 25px;
    }
    .home .home-content .text-2{
        font-size: 70px;
    }
    .home .home-content .text-3{
        font-size: 35px;
    }
    .home .home-content a{
        font-size: 23px;
        padding: 10px 30px;
    }
    .max-width{
        max-width: 930px;
    }
    .about .about-content .column{
        width: 100%;
    }
    .about .about-content .left{
        display: flex;
        justify-content: center;
        margin: 0 auto 60px;
    }
    .about .about-content .right{
        flex: 100%;
    }
    .education .edu-content .card{
        width: calc(50% - 10px);
        margin-bottom: 20px;
    }
    .skills .skills-content .column,
    .future .fp-content .column{
        width: 100%;
        margin-bottom: 35px;
    }
}

@media (max-width: 690px) {
    .max-width{
        padding: 0 23px;
    }
    .home .home-content .text-2{
        font-size: 60px;
    }
    .home .home-content .text-3{
        font-size: 32px;
    }
    .home .home-content a{
        font-size: 20px;
    }
    .education .edu-content .card{
        width: 100%;
    }
}

@media (max-width: 500px) {
    .home .home-content .text-2{
        font-size: 50px;
    }
    .home .home-content .text-3{
        font-size: 27px;
    }
    .about .about-content .right .text,
    .skills .skills-content .left .text{
        font-size: 19px;
    }
    .future .right form .fields{
        flex-direction: column;
    }
    .future .right form .name,
    .future .right form .email{
        margin: 0;
    }
    .right form .error-box{
       width: 150px;
    }
    .scroll-up-btn{
        right: 15px;
        bottom: 15px;
        height: 38px;
        width: 35px;
        font-size: 23px;
        line-height: 38px;
    }
    
}
</style>

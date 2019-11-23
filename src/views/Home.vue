<template>
  <div class="home">
    <div id="particles-js"></div>
        <h3 style="margin-top: 10vh;">Merry Chrimbus</h3>

    <div class="santaBackground">
      <santa style="max-width:300px;max-height:310px"/>
          <div id="ho"><h3 style="color:black;">HO HO HO</h3></div>

    </div>
  </div>
</template>
<script> 
import HelloWorld from '@/components/HelloWorld.vue'
import santa from '@/components/santa.vue'
import 'particles.js'
export default {

  name: 'home',
  components: {
    santa
  },
  mounted() {
    this.initParticles()
  },
  methods: {
    initParticles() {
      window.particlesJS("particles-js", {
      particles: {
        "number": {
          "value": 60,
          "density": {
            "enable": true,
            "value_area": 600
          }
        },
        "color": {
          "value": "#ffffff"
        },
        "shape": {
          "type": "circle",
          "stroke": {
            "width": 0,
            "color": "#000000"
          },
          "polygon": {
            "nb_sides": 5
          },
          "image": {
            "src": "img/github.svg",
            "width": 100,
            "height": 100
          }
        },
        "opacity": {
          "value": 0.5,
          "random": true,
          "anim": {
            "enable": false,
            "speed": 1,
            "opacity_min": 0.1,
            "sync": false
          }
        },
        "size": {
          "value": 5,
          "random": true,
          "anim": {
            "enable": false,
            "speed": 40,
            "size_min": 0.1,
            "sync": false
          }
        },
        "line_linked": {
          "enable": false,
          "distance": 789.1476416322727,
          "color": "#a78d12",
          "opacity": 0.4,
          "width": 1
        },
        "move": {
          "enable": true,
          "speed": 1,
          "direction": "bottom",
          "random": false,
          "straight": false,
          "out_mode": "out",
          "bounce": false,
          "attract": {
            "enable": false,
            "rotateX": 600,
            "rotateY": 1200
          }
        }
      },
      interactivity: {
        "detect_on": "canvas",
        "events": {
          "onhover": {
            "enable": false,
            "mode": "bubble"
          },
          "onclick": {
            "enable": true,
            "mode": "push"
          },
          "resize": true
        },
        "modes": {
          "grab": {
            "distance": 400,
            "line_linked": {
              "opacity": 1
            }
          },
          "bubble": {
            "distance": 400,
            "size": 40,
            "duration": 2,
            "opacity": 8,
            "speed": 3
          },
          "repulse": {
            "distance": 200,
            "duration": 0.4
          },
          "push": {
            "particles_nb": 4
          },
          "remove": {
            "particles_nb": 2
          }
        }
      },
      retina_detect: false
    })
    }
  }
};
</script>


<style lang="scss" scoped>
@import url('https://fonts.googleapis.com/css?family=Mountains+of+Christmas&display=swap');
.home{
  h3{
    color: white;
    font-family: 'Mountains of Christmas', cursive;
    font-size: 2rem;

  }
}
.santaBackground{
  overflow: hidden;
  width: 300px;
  height: 300px;
  margin: 0 auto;
  border-radius: 50%;
  background-color: mediumturquoise;
}
#ho{
  overflow: show !important;
  animation: hideShow 1s linear infinite alternate forwards;
  background-color: white;
  width: 150px;
  position: relative;
  top: -330px;
  left: 5%;
  border-radius: 55px;
  transform: rotate(-30deg)

}
@keyframes hideShow {
  to{
    opacity: 0;
  }
  from{
    opacity: 1;
  }
}
 #particles-js {
    background:rgb(179, 13, 13);
    position: fixed;
    height: 100vh;
    width: 100vw;
    top: 0;
    left: 0;
    margin: 0;
    padding: 0;
    z-index: -1;
  }

</style>

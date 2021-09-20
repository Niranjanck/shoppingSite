<template>
  <div>
    <!-- home menu -->

    <div class="mainHome relative bg-cover bg-center">
      <div class="main flex">
        <!-- side image -->
        <div class="sideImage absolute inset-x-0 top-20 left-5"></div>
        <!-- home qoutes -->
        <div class="sideLetter absolute top-20">
          <svg viewBox="0 0 1350 600">
            <text x="10%" y="80%" fill="transparent">SHOP NOW</text>
          </svg>
        </div>
      </div>
      <div class="slider absolute">
        <v-slide-group multiple show-arrows>
          <v-slide-item v-for="(slide, i) in slides" :key="i">
            <v-card elevation="2" class="cardd"> </v-card>
          </v-slide-item>
        </v-slide-group>
      </div>
    </div>

    <!-- section two -->
    <div class="secondSection bg-cover">
      <h1 class="category">CATEGORY</h1>
      <v-container class="pa-4 text-center">
        <v-row class="fill-height" align="center" justify="center">
          <template v-for="(item, i) in items">
            <v-col :key="i" cols="12" md="4">
              <v-hover v-slot="{ hover }">
                <v-card
                  class="imageCard"
                  :elevation="hover ? 12 : 2"
                  :class="{ 'on-hover': hover }"
                >
                  <v-img :src="item.img" height="225px">
                    <v-card-title class="text-h6 white--text">
                      <v-row
                        class="fill-height flex-column"
                        justify="space-between"
                      >
                        <p class="mt-4 subheading text-left">
                          {{ item.title }}
                        </p>

                        <div>
                          <p
                            class="
                              text-caption
                              font-weight-medium font-italic
                              text-left
                            "
                          >
                            {{ item.subtext }}
                          </p>
                        </div>

                        <div class="align-self-center">
                          <v-btn class="showBtn" elevation="2"> Shop now</v-btn>
                        </div>
                      </v-row>
                    </v-card-title>
                  </v-img>
                </v-card>
              </v-hover>
            </v-col>
          </template>
        </v-row>
      </v-container>
    </div>

    <!-- footer -->

    <div>
      <v-footer dark padless>
        <v-card class="flex" flat tile>
          <v-card-title>
            <strong class="subheading"
              >Get connected with us on social networks!</strong
            >

            <v-spacer></v-spacer>

            <v-btn v-for="icon in icons" :key="icon" class="mx-4" dark icon>
              <v-icon size="24px">
                {{ icon }}
              </v-icon>
            </v-btn>
          </v-card-title>
          <v-divider></v-divider>

          <v-card-text class="py-2 white--text text-center">
            {{ new Date().getFullYear() }} — <strong>SHOP</strong>
          </v-card-text>
        </v-card>
      </v-footer>
    </div>
  </div>
</template>
<style scoped>
.showBtn {
  background-color: rgb(38, 0, 255);
  color: white;
}
p {
  color: white;
}

.imageCard {
  transition: opacity 0.4s ease-in-out;
}
.imageCard:not(.on-hover) {
  opacity: 0.6;
}

.gridCard {
  background-color: white;
  width: 200px;
  height: 200px;
  margin: 20px;
  border-radius: 9px;
}

.category {
  padding-top: 55px;
  font-size: 36px;
  text-align: center;
}
.cardd {
  width: 100px;
  height: 100px;
  margin: 10px;
  background-color: red;
}

.slider {
  width: 100%;
  margin: auto;
  padding: 5px;
  transform: translate(-50%, -50%);
  left: 50%;
  top: 70%;
}
.mainHome {
  background-image: url('assets/img/RED.svg');
  height: 500px;
  width: 100%;
}
.secondSection {
  background-image: url('assets/img/second.svg');
  height: auto;
}
.sideImage {
  width: 200px;
  background-image: url('assets/img/fashion1.svg');
  height: 200px;
}
.sideLetter {
  left: 76%;
  top: 50%;
  transform: translate(-52%, -185%);
  width: 161px;
  height: 100px;
}
svg text {
  stroke: black;
  font-size: 200px;
  font-weight: 800;
  stroke-width: 5;
  animation: textAnimate 8s;
}
@keyframes textAnimate {
  0% {
    stroke-dasharray: 0 50%;
    stroke-dashoffset: 20%;
    fill: red;
  }
  100% {
    stroke-dasharray: 50% 0;
    stroke-dashoffset: -20%;
  }
}
@media (min-width: 480px) {
  .gridCard {
    width: 350px;
    height: 350px;
    background-color: rgb(255, 255, 255);
    margin: 20px;
  }
  .cat {
    width: 800px;
    margin: auto;
  }
  svg text {
    font-size: 220px;
  }
  .sideLetter {
    left: 80%;
    top: 50%;
    transform: translate(-90%, -185%);
    width: 218px;
    height: 100px;
  }
}

@media (min-width: 652px) {
  .sideLetter {
    left: 66%;
    top: 53%;
    transform: translate(-66%, -185%);
    width: 300px;
    height: 100px;
  }
  svg text {
    font-size: 220px;
  }
  .slider {
    width: 500px;
    transform: translate(-44%, -50%);
    left: 58%;
    top: 70%;
  }
  .sideImage {
    width: 250px;
    height: 250px;
  }
}
@media (min-width: 880px) {
  .sideImage {
    width: 400px;
    height: 400px;
  }
  .sideLetter {
    left: 59%;
    top: 53%;
    transform: translate(-52%, -185%);
    width: 300px;
    height: 100px;
  }
  svg text {
    font-size: 210px;
  }
  .slider {
    width: 500px;
    margin: auto;
    padding: 5px;
    transform: translate(-8%, -50%);
    left: 50%;
    top: 70%;
  }
  .cardd {
    width: 150px;
    height: 150px;
  }
}
@media (min-width: 1160px) {
  .sideImage {
    width: 400px;
    height: 400px;
    margin: 40px;
  }
  .cardd {
    width: 150px;
    height: 150px;
  }
  svg text {
    font-size: 200px;
  }
  .slider {
    transform: translate(20%, -20%);
    left: 40%;
    top: 80%;
    width: 600px;
  }
  .sideLetter {
    transform: translate(-60%, -20%);
    left: 60%;
    top: 20%;
    width: 500px;
  }
  .sideImage {
    width: 400px;
    height: 400px;
  }
}
@media (min-width: 1579px) {
  .cardd {
    width: 200px;
    height: 200px;
  }
  .slider {
    width: 800px;
    margin-left: 5px;
    transform: translate(-80%, -80%);
    top: 80%;
    left: 80%;
  }
  .sideImage {
    width: 860px;
    height: 670px;
  }
  .sideLetter {
    width: 1400px;
    height: 600px;
  }
  .mainHome {
    height: 100vh;
  }
  svg text {
    stroke: black;
    font-size: 120px;
    font-weight: 800;
    stroke-width: 5;
    animation: textAnimate 8s;
    transform: translate(30%, -50%);
    left: 30%;
    top: 50%;
  }
}
</style>

<script>
export default {
  data() {
    return {
      slides: ['1', '2', '3', '4', '5', '6', '7', '8', '9', '10'],
      icons: ['mdi-facebook', 'mdi-twitter', 'mdi-linkedin', 'mdi-instagram'],
      items: [
        {
          title: 'New Releases',
          subtext: 'Newly released songs. Updated daily.',
          img: 'https://images.unsplash.com/photo-1429514513361-8fa32282fd5f?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=3264&q=80',
        },
        {
          title: 'Rock',
          subtext: 'Lose yourself in rock tunes.',
          img: 'https://images.unsplash.com/photo-1498038432885-c6f3f1b912ee?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=2100&q=80',
        },
        {
          title: 'Mellow Moods',
          subtext: 'Chill beats to mellow you out.',
          img: 'https://images.unsplash.com/photo-1542320868-f4d80389e1c4?ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&ixlib=rb-1.2.1&auto=format&fit=crop&w=3750&q=80',
        },
      ],
      transparent: 'rgba(255, 255, 255, 0)',
    }
  },
}
</script>

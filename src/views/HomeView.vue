<template>
  <v-app id="home">
    <Navbar />
    <v-container fluid>
      <div class="head">
        <v-row>
          <v-col cols="5">
            <div style="position: relative;" class="mt-16">
              <h1 class="text-grey">Hello,</h1>
              <h1 class="text-grey">I'm Thuan Phat</h1>
              <span class="text-grey">Web Designer & Developer</span><br />
              <v-btn tile class="text-blue-darken-4 mt-8" variant="outlined">
                Contact me
              </v-btn>
            </div>
          </v-col>
          <v-col cols="2">
            <div
              style="position: absolute; z-index: 999; bottom: 0;margin:auto 0; left: 0; right: 0; text-align: center;">
              <v-icon>fas fa-angle-double-down</v-icon>
            </div>
          </v-col>
          <v-col cols="5" style="position: relative; z-index: 999; " class="mt-16">
            <v-img src="i1.png" contain max-height="300"></v-img>
          </v-col>
        </v-row>
      </div>
      <v-col cols="12" class="mt-16" id="about">
        <div>
          <v-row>
            <v-col cols="12" sm="6">
              <div class="egg">
                <v-img src="i2.png" max-height="300"></v-img>
              </div>
            </v-col>
            <v-col cols="12" sm="6">
              <h5 class="mt-16">About me</h5>
              <div style="width:120px">
                <v-slider v-model="slider2" color="blue-darken-4" track-color=""></v-slider>
              </div>
              <h4 class="mt-n4">I am a Creative Web Design</h4>
              <h4>And Developer</h4>
              <p class="text-grey">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quidem nobis neque quasi
                commodi tenetur praesentium? Assumenda consectetur repellendus pariatur veniam nisi. Fugiat consequuntur
                laudantium dolorum obcaecati deserunt ipsum velit ab!</p>
              <br />
              <p class="text-grey">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Quidem nobis neque quasi
                commodi tenetur praesentium? Assumenda consectetur repellendus pariatur veniam nisi. Fugiat consequuntur
                laudantium dolorum obcaecati deserunt ipsum velit ab!</p>
              <v-btn tile dark color="blue-darken-4" class="mt-4">Download Resume</v-btn>
            </v-col>
          </v-row>
        </div>

      </v-col>
      <div class="text-center mt-4">
        <h2>What We Do</h2>
        <div style="width: 120px; margin: 0 auto;">
          <v-slider v-model="slider2" color="blue-darken-4" track-color=""></v-slider>
        </div>
      </div>
    </v-container>

  </v-app>
</template>

<script>
import { defineComponent } from "vue";

// Components
import Navbar from "../components/NavBar.vue";

export default defineComponent({
  name: "HomeView",
  setup() {
    return {
      slider2: 50,
      items: [
        {
          img: "i3.jpg"
        },
        {
          img: "i4.jpg"
        },
        {
          img: "i5.jpg"
        },
        {
          img: "i6.jpg"
        },
        {
          img: "i9.jpg"
        },
        {
          img: "i8.jpg"
        },
      ]
    }
  },

  components: {
    Navbar,
  },
});
</script>
<style scoped>
.v-container {
  padding: 16px 0;
}

.head {
  position: relative;
  text-align: center;
  padding: 12px;
  margin-bottom: 6px;
  height: 400px;
  width: 100%;
  color: white;
}

.head::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 50%;
  background: black;
  transform: skew(0deg, 6deg);
}

.head::after {
  content: "";
  position: absolute;
  top: 0;
  right: 0;
  height: 100%;
  width: 50%;
  background: black;
  transform: skew(0deg, -6deg);
}

.egg {
  display: block;
  margin-left: 100px;
  margin-top: 50px;
  width: 356px;
  height: 300px;
  background-color: #0D47A1;
  border-radius: 50% 50% 50% 50% / 60% 60% 40% 40%;
}
</style>

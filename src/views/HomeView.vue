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
      <v-col cols="12" class="padd" id="portfolio">
        <div class="first" id="project">
          <v-row>
            <v-col cols="12">
              <div class="child">
                <v-btn icon="fas fa-laptop" color="blue-darken-4" class="text-white"></v-btn>
                <h3 class="ml-3 mt-4">Web design</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                  Lorem ipsum dolor, sit amet <br /> adipisicing elit. Facilis, maxime?
                </p>
              </div>
              <div class="child">
                <v-btn icon="fas fa-mobile-alt" color="blue-darken-4" class="text-white"></v-btn>
                <h3 class="ml-3 mt-4">App design</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                  Lorem ipsum dolor, sit amet <br /> adipisicing elit. Facilis, maxime?
                </p>
              </div>
              <div class="child">
                <v-btn icon="fas fa-camera" color="blue-darken-4" class="text-white"></v-btn>
                <h3 class="ml-3 mt-4">Photography</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                  Lorem ipsum dolor, sit amet <br /> adipisicing elit. Facilis, maxime?
                </p>
              </div>
              <v-divider></v-divider>
            </v-col>
          </v-row>
        </div>
      </v-col>
      <v-col cols="12" sm="12" id="services" class="mt-12">
        <div class="d-flex justify-center mb-6">
          <v-btn color="blue-darken-4" class="mr-2">All</v-btn>
          <v-btn class="mr-2" variant="tonal">Web Design</v-btn>
          <v-btn class="mr-2" variant="tonal">Fron Design</v-btn>
          <v-btn class="mr-2" variant="tonal">Photography</v-btn>
          <v-btn variant="tonal">Illustration</v-btn>
        </div>
      </v-col>
      <v-col cols="12" class="imgHover">
        <v-row class="fill-height" align="center" justify="center">
          <template v-for="(item, i) in items" :key="i">
            <v-col cols="12" md="4">
              <v-hover v-slot="{ isHoverimg, props }">
                <v-card :elevation="isHoverimg ? 12 : 2" class="{'on-hover' : isHoverimg}" v-bind="props">
                  <v-img :src="item.img" height="225px" cover></v-img>
                </v-card>
              </v-hover>
            </v-col>
          </template>
        </v-row>
      </v-col>
      <v-col cols="12" sm="12">
        <div class="d-flex justify-center mb-6">
          <v-btn color="blue-darken-4" class="mr-4">Load More</v-btn>
        </div>
      </v-col>
      <v-col cols="12" id="page">
        <div class="pre">
          <v-row>
            <v-col cols="12" sm="4">
              <v-card class="mx-auto" max-height="344" height="">
                <v-img src="i10.jpg" height="200px" cover></v-img>
                <v-card-title>We provide you the best</v-card-title>
                <v-card-subtitle>By thphat | 13 Feb 2023</v-card-subtitle>
                <v-card-text>Lorem ipsum dolor sit amet consectetur adipisicing elit. Repellendus magni consectetur
                  animi maiores enim culpa sed illum, reprehenderit corporis in totam, numquam at quis non consequatur
                  quibusdam quidem quo rerum?</v-card-text>
              </v-card>
            </v-col>
            <v-col cols="12" sm="4">
              <v-card class="mx-auto" max-height="344" height="">
                <v-img src="i11.jpg" height="200px" cover></v-img>
                <v-card-title>We provide you the best</v-card-title>
                <v-card-subtitle>By thphat | 13 Feb 2023</v-card-subtitle>
                <v-card-text>Lorem ipsum dolor sit amet consectetur adipisicing elit. Repellendus magni consectetur
                  animi maiores enim culpa sed illum, reprehenderit corporis in totam, numquam at quis non consequatur
                  quibusdam quidem quo rerum?</v-card-text>
              </v-card>
            </v-col>
            <v-col cols="12" sm="4">
              <v-card class="mx-auto" max-height="344" height="">
                <v-img src="i12.jpg" height="200px" cover></v-img>
                <v-card-title>We provide you the best</v-card-title>
                <v-card-subtitle>By thphat | 13 Feb 2023</v-card-subtitle>
                <v-card-text>Lorem ipsum dolor sit amet consectetur adipisicing elit. Repellendus magni consectetur
                  animi maiores enim culpa sed illum, reprehenderit corporis in totam, numquam at quis non consequatur
                  quibusdam quidem quo rerum?</v-card-text>
              </v-card>
            </v-col>
          </v-row>
        </div>
      </v-col>
      <v-col cols="12" id="blog">
        <div class="hire">
          <v-row>
            <v-col cols="12" sm="8">
              <h1 class="mt-9">Hire me for your awesome project</h1>
              <p class="text-grey">
                Lorem ipsum, dolor sit amet consectetur adipisicing elit. Repudiandae voluptates iure ratione.
                Voluptate, aliquam quibusdam, neque, hic enim a eius rerum perspiciatis nostrum fuga molestias nemo
                quasi praesentium repudiandae ea?
              </p>
            </v-col>
            <v-col cols="12" sm="4">
              <v-btn color="blue-darken-4" class="mt-15">Hire me</v-btn>
            </v-col>
          </v-row>
        </div>
      </v-col>
      <v-col cols="12" sm="12" class="px-16" id="contact">
        <v-row>
          <v-col cols="12" sm="4">
            <div class="child">
              <h1>Contact info.</h1>
              <v-btn icon="fas fa-map-marker-alt" class="mt-10" variant="outlined"></v-btn> <br />
              <span class="text-caption">
                Your Street SYO, Your Area Dream
              </span> <br />
              <v-btn icon="fas fa-phone-alt" class="mt-10" variant="outlined"></v-btn><br />
              <span class="text-caption">
                099999999
              </span> <br />
              <span class="text-caption">
                012345678
              </span> <br />
              <v-btn icon="fas fa-envelope" class="mt-10" variant="outlined"></v-btn><br />
              <span class="text-caption">
                thphatt@gmail.com
              </span> <br />
              <span class="text-caption">
                thphatt@gmail.com
              </span> <br />
            </div>
          </v-col>
          <v-col cols="12" sm="8">
            <h1 class="mt-8">Send your message</h1>
            <v-divider></v-divider>
            <span class="text-caption">
              Lorem ipsum dolor sit amet consectetur, adipisicing elit. Id delectus minima quisquam ipsam, quibusdam
              vitae nulla magni dicta. Ratione vitae ex at laudantium minus necessitatibus? Ipsa, blanditiis. Itaque,
              laboriosam tempora.
            </span>
            <v-row class="mt-10">
              <v-col cols="12" sm="6">
                <v-text-field label="Name" persistent-hint variant="outlined"></v-text-field>
              </v-col>
              <v-col cols="12" sm="6">
                <v-text-field label="Phone" persistent-hint variant="outlined"></v-text-field>
              </v-col>
            </v-row>
            <v-textarea label="Message" persistent-hint variant="outlined"></v-textarea>
            <v-btn color="blue-darken-4" class="mt-2">Submit now</v-btn>
          </v-col>
        </v-row>
      </v-col>
    </v-container>
    <FooterView />
  </v-app>
</template>

<script>
import {
  defineComponent
} from "vue";

// Components
import Navbar from "../components/NavBar.vue";
import FooterView from "../components/FooterView.vue";
export default defineComponent({
  name: "HomeView",
  setup() {
    return {
      slider2: 50,
      items: [{
        img: "i3.jpg"
      },
      {
        img: "i4.jpg"
      },
      {
        img: "i5.jpg"
      },
      {
        img: "i6.jpeg"
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
    FooterView
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

.first {
  width: 100%;
  height: 200px;
  text-align: center;
  padding: 2rem;
}

.child {
  display: inline-block;
  padding: 2rem 1rem;
  vertical-align: middle;
  text-align: center;
  margin-right: 8px;

}

.imgHover {
  padding: 0 200px;
}

.pre {
  width: 100%;
  height: 380px;
  text-align: center;
  padding: 0 200px;
  background-color: #f5f5f5;
}



.hire {
  width: 100%;
  height: 200px;
  padding: 0 200px;
  background-color: #e9e9e9;
  margin-top: -24px;
}
</style>

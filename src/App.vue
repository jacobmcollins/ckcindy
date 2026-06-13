<template>
  <v-app>
      <v-app-bar app color="white" flat>
        <v-app-bar-title>
          <img src="./assets/CKC5.PNG" class="logo" alt="Courage & Kindness Co" />
        </v-app-bar-title>
        <!-- <template v-slot:prepend>
          <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>
        </template> -->
        <v-btn icon="mdi-email" color="#666" href="mailto:info@ckcindy.org">
        </v-btn>
        <v-btn icon="mdi-facebook" color="#1877F2" href="https://www.facebook.com/courageandkindnessco">
        </v-btn>
        <v-btn  icon="mdi-instagram" color="#E1306C" href="https://www.instagram.com/courageandkindnessco">
        </v-btn>
        <v-btn base-color="red" rounded variant="tonal" href="https://givebutter.com/support-ckc-indy" target="_blank">
          <template v-slot:prepend>
            <v-icon>mdi-heart</v-icon>
          </template>
          DONATE
        </v-btn>
      </v-app-bar>

      <v-navigation-drawer v-model="drawer" temporary location="top">
        <v-list>
          <v-list-item @click="goToHome">Home</v-list-item>
          <v-list-item @click="goToAboutUs">About Us</v-list-item>
        </v-list>
      </v-navigation-drawer>

      <v-main class="main-bg">
        <v-sheet class="about-sheet">
          <v-card-title class="text-black text-center about-title">About Us</v-card-title>
          <v-card-text class="text-body-1 text-black text-center">
            Courage & Kindness Co. provides the magic of meeting beloved fairytale characters to local nonprofits, hospitals, and the community. At no charge, children in difficult circumstances are given the opportunity to make priceless memories with their favorite characters. CKC specializes in unique experiences tailored to individual children, but also works closely with Down Syndrome Indiana, multiple autism centers, the UMDF, Peyton Manning Children's Hospital, and other local organizations.
          </v-card-text>
        </v-sheet>
        <div class="instagram-feed">
          <behold-widget feed-id="pdEDR4FM2jDy7rrY2GgX"></behold-widget>
        </div>
        <!-- <v-container fluid class="page">
          <div class="about-card">
            <v-card class="pa-1 opacity-70" max-width="640" elevation="10">
              <v-card-title class="text-h5">About Us</v-card-title>
              <v-card-text>
                Courage & Kindness Co. provides the magic of meeting beloved fairytale characters to local nonprofits, hospitals, and the community. At no charge, children in difficult circumstances are given the opportunity to make priceless memories with their favorite characters. CKC specializes in unique experiences tailored to individual children, but also works closely with Down Syndrome Indiana, multiple autism centers, the UMDF, Peyton Manning Children's Hospital, and other local organizations.
              </v-card-text>
            </v-card>
          </div>
            <v-carousel class="instagram-card" hide-delimiters>
              <v-carousel-item
                  src="https://cdn.vuetifyjs.com/images/cards/docks.jpg"
                ></v-carousel-item>

                <v-carousel-item
                  src="https://cdn.vuetifyjs.com/images/cards/hotel.jpg"
                ></v-carousel-item>

                <v-carousel-item
                  src="https://cdn.vuetifyjs.com/images/cards/sunshine.jpg"
                ></v-carousel-item>
            </v-carousel>
        </v-container> -->
      </v-main>
  </v-app>
</template>

<script setup lang="ts">
import { ref, onMounted } from 'vue';

onMounted(() => {
  const s = document.createElement('script');
  s.type = 'module';
  s.src = 'https://w.behold.so/widget.js';
  document.head.append(s);
});

const drawer = ref<Boolean>(true);

const goToHome = () => {
  drawer.value = false;
};

const goToAboutUs = () => {
  drawer.value = false;
};
</script>

<style scoped>
.main-bg {
  min-height: 100vh;
  background-image: url("./assets/DSC_0798.JPG");
  background-size: cover;
  background-position: center;
  background-attachment: fixed;
}

.about-sheet {
  background-color: rgba(255, 255, 255, 0.8) !important;
  margin: 32px auto;
  border-radius: 8px;
  max-width: 900px;
}

.about-sheet :deep(.v-card-text) {
  font-family: 'Rosarivo', serif !important;
}

.about-title {
  font-family: 'Passions Conflict', cursive !important;
  font-size: 4rem !important;
}

.instagram-feed {
  margin: 16px;
}

.instagram-feed behold-widget {
  --behold-border: none;
  border: none !important;
}

.logo {
  height: 48px;
  width: auto;
  mix-blend-mode: multiply;
}

</style>

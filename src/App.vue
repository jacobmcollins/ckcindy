<template>
  <!-- Full-page background -->
  <v-container fluid class="page">
    <!-- Optional dark overlay for readability -->
    <div class="overlay"></div>

    <!-- Card wrapper: centered horizontally, near top -->
    <div class="card-wrap">
      <v-card class="pa-1 opacity-70" max-width="640" elevation="10">
        <v-card-title class="text-h5">About Us</v-card-title>
        <v-card-text>
          Courage & Kindness Co. provides the magic of meeting beloved fairytale characters to local nonprofits, hospitals, and the community. At no charge, children in difficult circumstances are given the opportunity to make priceless memories with their favorite characters. CKC specializes in unique experiences tailored to individual children, but also works closely with Down Syndrome Indiana, multiple autism centers, the UMDF, Peyton Manning Children's Hospital, and other local organizations.
        </v-card-text>
        <v-list>
          <v-list-item href="mailto:info@ckcindy.org">
            <template v-slot:prepend>
              <v-avatar>
                <v-icon icon="mdi-email"></v-icon>
              </v-avatar>
            </template>
            <v-list-item-title>info@ckcindy.org</v-list-item-title>
            <v-list-item-subtitle>Email</v-list-item-subtitle>
          </v-list-item>
          <v-list-item href="https://www.facebook.com/courageandkindnessco">
            <template v-slot:prepend>
              <v-avatar>
                <v-icon icon="mdi-facebook"></v-icon>
              </v-avatar>
            </template>
            <v-list-item-subtitle>Facebook</v-list-item-subtitle>
          </v-list-item>
          <v-list-item href="https://www.instagram.com/courageandkindnessco">
            <template v-slot:prepend>
              <v-avatar>
                <v-icon icon="mdi-instagram"></v-icon>
              </v-avatar>
            </template>
            <v-list-item-subtitle>Instagram</v-list-item-subtitle>
          </v-list-item>
        </v-list>
      </v-card>
    </div>
  </v-container>
</template>

<style scoped>
/* Full viewport background image */
.page {
  min-height: 100vh;
  position: relative;
  background-image: url("./assets/background.jpg"); /* put your image in /public/images/bg.jpg */
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}

/* Optional overlay to improve contrast */
.overlay {
  position: absolute;
  inset: 0;
  background: rgba(0, 0, 0, 0.35);
}

/* Center horizontally, but keep near the top */
.card-wrap {
  position: relative; /* above overlay */
  z-index: 1;

  display: flex;
  justify-content: center;

  padding-top: 48px;   /* distance from top */
  padding-left: 16px;  /* mobile breathing room */
  padding-right: 16px;

}
</style>

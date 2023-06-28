<style lang="scss">
body {
  /*wallpaper adaptation found on css tricks*/
  background: url(public/images/wallpaper.jpg) no-repeat center center fixed;
  background-size: cover;
  -webkit-background-size: cover;
  -o-background-size: cover;
  -moz-background-size: cover;
}
.citation-heading {
  //   margin: 0 12px;
  //   text-align: center;
  max-width: 350px;
}
</style>

<template>
  <!-- grid wrapper -->
  <div class="flex-grow column items-center justify-center grid-wrapper">
    <!-- Home page contained in a div and managed with a grid -->
    <div class="home-grid row">
      <q-card class="citation-div">
        <h5 class="citation-heading">
          <b
            >" Lorem Ipsum is simply dummy text of the printing and typesetting
            industry.<br />
            Lorem Ipsum has been the industry's standard dummy text ever since
            the 1500s, when an unknown printer took a galley of type and
            scrambled it to make a type specimen book. "</b
          >
        </h5>
      </q-card>

      <q-list>
        <q-item>
          <q-btn
            color="secondary"
            icon-right="school"
            label="Corsi"
            class="courses-button"
          />
        </q-item>

        <q-item>
          <q-btn
            color="secondary"
            icon-right="info"
            label="About"
            class="about-button"
          />
        </q-item>

        <q-item>
          <q-btn
            color="secondary"
            icon-right="people"
            label="Contatti"
            class="contact-button"
          />
        </q-item>
      </q-list>
    </div>
  </div>
</template>

<script setup lang="ts"></script>

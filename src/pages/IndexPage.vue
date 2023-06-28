<style lang="scss">
.row {
  display: flex;
  flex-direction: row;
}

.column {
  display: flex;
  flex-direction: column;
}

.flex-grow {
  flex-grow: 1;
}

.justify-evenly {
  justify-content: space-evenly;
}

.justify-center {
  justify-content: center;
}

.items-center {
  align-items: center;
}

/*~~||~~||~~||~~||~~||~~||~~||~~||~~||~~||~~||~~||~~||~~||~~||~~||~~||~~||~~||~~||~~||~~||~~||~~||~~||~~||~~||~~||~~*/

/*--------------Home-Grid--------------*/
.citation-div {
  display: flex;
  background-color: rgba(255, 255, 255, 0.5);
  backdrop-filter: blur(15px);
  border-radius: 25px;
  place-self: center;
  /* indicates the occupied area (from row 1 col 1, to row 3 col 1) */
  grid-area: 1/1/4/1;
  /* adapt the div to the area in which is contained */
  align-self: stretch;
  /* align contained items on the y axe */
  align-items: center;
}

.grid-wrapper {
  padding: 24px;
}

.citation-heading {
  margin: 0 12px;
  text-align: center;
}

.home-grid {
  column-gap: 24px;
  display: grid;
  grid-template-columns: 0.3fr 0.5fr;
  justify-content: center;
  row-gap: 24px;

  @media (width < 900px) {
    grid-template-columns: 350px;
    grid-template-rows: repeat(6, 100px[row-start]);
  }
}

.contact-button {
  backdrop-filter: blur(15px);
  background-color: rgba(89, 124, 43, 0.5);
  grid-row: 3;

  @media (width < 900px) {
    grid-row: 6;
    grid-column: 1;
  }
}
</style>

<template>
  <!-- grid wrapper -->
  <div
    id="homeWrapperRef"
    class="flex-grow column items-center justify-center grid-wrapper"
  >
    <!-- Home page contained in a div and managed with a grid -->
    <div id="homeWrapperRef" class="home-grid">
      <div id="citationDivRef" class="citation-div">
        <h2 id="citationHeadingRef" class="citation-heading">
          <b
            >" Lorem Ipsum is simply dummy text of the printing and typesetting
            industry.<br />
            Lorem Ipsum has been the industry's standard dummy text ever since
            the 1500s, when an unknown printer took a galley of type and
            scrambled it to make a type specimen book. "</b
          >
        </h2>
      </div>

      <q-btn
        color="secondary"
        icon-right="school"
        label="Corsi"
        class="courses-button"
      />

      <q-btn
        color="secondary"
        icon-right="info"
        label="About"
        class="about-button"
      />

      <q-btn
        color="secondary"
        icon-right="people"
        label="Contatti"
        class="contact-button"
      />
    </div>
  </div>
</template>

<script setup lang="ts">
import { Todo, Meta } from 'components/models';
import ExampleComponent from 'components/ExampleComponent.vue';
import { ref } from 'vue';

const todos = ref<Todo[]>([
  {
    id: 1,
    content: 'ct1',
  },
  {
    id: 2,
    content: 'ct2',
  },
  {
    id: 3,
    content: 'ct3',
  },
  {
    id: 4,
    content: 'ct4',
  },
  {
    id: 5,
    content: 'ct5',
  },
]);
const meta = ref<Meta>({
  totalCount: 1200,
});
</script>

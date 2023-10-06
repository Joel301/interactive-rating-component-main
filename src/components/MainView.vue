<script setup>
import { ref } from 'vue'
import { useRouter } from 'vue-router'
const router = useRouter()
import StartLogo from './icons/IconStar.vue'
const selection = ref(0)
</script>

<template>
  <header>
    <div class="clearCircularButton starContainer">
      <StartLogo />
    </div>
    <h1>How did we do?</h1>
  </header>
  <section>
    <p>
      Please let us know how we did with your support request. All feedback is appraciated to help
      us improve our offering!
    </p>
    <ul class="ratingContainer">
      <li v-for="rat in 5">
        <button
          @click.prevent="selection = rat"
          :class="{
            clearCircularButton: true,
            selected: selection == rat
          }"
        >
          {{ rat }}
        </button>
      </li>
    </ul>
    <button
      class="btnSubmit"
      @click.prevent="router.push(`/thankyou/${selection+1}`)">SUBMIT</button>
  </section>
</template>

<style>
.ratingContainer {
  padding: 0;
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr 1fr;
  justify-items: center;
}

.ratingContainer > li {
  display: contents;
  background-color: var(--Dark-Blue);
  justify-items: center;
  height: 18px;
  width: 20px;
}

.clearCircularButton {
  background-color: var(--someColor);
  border: none;
  border-radius: 50%;
  width: 45px;
  padding: 2ex;
  text-align: center;
  color: var(--Medium-Grey);
  font-family: Overpass;
  font-weight: 700;
}

.starContainer {
  width: 18px;
  height: 18px;
}
.btnSubmit {
  background-color: var(--Orange);
  color: var(--White);
  width: -webkit-fill-available;
  padding: 1em;
  border-radius: 3em;
  border: 0;
  letter-spacing: 2px;
}

.btnSubmit:hover {
  background-color: var(--White);
  color: var(--Orange);
}
li > .clearCircularButton:hover {
  background-color: var(--Orange);
  color: var(--White);
}

.selected {
  background-color: var(--Light-Grey);
  color: var(--White);
}
</style>

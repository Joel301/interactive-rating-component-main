<script setup>
import { useAttrs } from 'vue'
import IconThankYouVue from './icons/IconThankYou.vue'

const { rat } = useAttrs()
</script>

<template>
  <header>
    <div class="thankYouContainer">
      <IconThankYouVue />
    </div>
    <div class="selectionResult">You selected {{ rat }} out of 5</div>
  </header>
  <section class="thankSection">
    <h1>Thank you!</h1>
    <p>
      We appreciate you takin the time to give a rating. If you ever need more support, don't
      hesitate to get in touch!
    </p>
  </section>
</template>

<style>
.selectionResult {
  background-color: var(--someColor);
  color: var(--Orange);
  margin-top: 1rem;
  padding: 0.5em;
  padding-left: 1em;
  padding-right: 1em;
  border-radius: 1.5em;
}
.thankSection > h1 {
  margin-bottom: 5px;
}
.thankSection > p {
  align-items: center;
  text-align: center;
  margin: 0;
}
.thankSection {
  display: flex;
  flex-direction: column;
  align-items: center;
}
.thankYouContainer {
  display: block;
  margin-top: 1rem;
}
.mainContainer {
  display: flex;
  flex-direction: column;
  align-items: center;
  min-height: 310px;
  justify-content: space-evenly;
}
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

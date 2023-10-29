<script setup>

const msg = "Hello World";
const className = "is";
const id = "io";

const objectAttributes = {
  id: "io",
  classname: "isName",
  class: `${new Date()}`
}

const key = "href";
const url = "https://google.com/"

const Disabled = false;

</script>

<template>
  <h1> {{ msg }}</h1>
  <h1 v-bind:id="id"> {{ msg }} </h1>
  <h1 v-bind:class="id"> {{ msg }} </h1>
  <h1 v-bind:class="className" v-bind:id="id" > {{ msg }} </h1>
  <h1 :class="className" :id="id" > {{ msg }} </h1>
  <div v-bind="objectAttributes">

    <a :[key]="url"> click me </a>

    <button v-bind:disabled="Disabled"> click me </button>

  </div>
</template>
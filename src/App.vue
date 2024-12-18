<script setup lang="ts">
import HelloWorld from './components/HelloWorld.vue';
import FormBinding from './components/FormBinding.vue';
import EventListeners from './components/EventListeners.vue';
import ConditionalRendering from './components/ConditionalRendering.vue';
import ListRendering from './components/ListRendering.vue';
import ComputedProperty from './components/ComputedProperty.vue';
import LifecycleAndTemplateRefs from './components/LifecycleAndTemplateRefs.vue';
import Watchers from './components/Watchers.vue';
import Props from './components/Props.vue';
import Emits from './components/Emits.vue';


import { ref } from 'vue';

const message = ref('Hello World!');
const titleClass = ref('title');

function greetings(msg: string){
  message.value = msg;
}
 </script>

<template>
  <h1 :class="titleClass">{{ message }}</h1>

  <!--
    <EventListeners />
    <FormBinding/>
    <ConditionalRendering/>
    <ListRendering/>
    <ComputedProperty/>
    <LifecycleAndTemplateRefs/>
    <Watchers/>
    <Props :msg="'New count is '"/>

  -->
  <Emits @response="greetings"/>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
.title {
  color: red;
}
</style>

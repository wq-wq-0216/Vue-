<template>
  <div>

    <button @click="switchView('HelloWorld')">切换到 HelloWorld</button>
    <button @click="switchView('TheWelcome')">切换到 TheWelcome</button>
    <button @click="switchView('WelcomeItem')">切换到 WelcomeItem</button>

    <keep-alive :include="['HelloWorld', 'TheWelcome']">
      <component :is="view"></component>
    </keep-alive>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue';
import TheWelcome from './components/TheWelcome.vue';
import WelcomeItem from './components/WelcomeItem.vue';

  export default {
    data() {
      return {
        view: 'HelloWorld'
      }
    },
    methods: {
      switchView(name) {
        this.view = name
      }
    },
    components: {
      HelloWorld, TheWelcome, WelcomeItem
    }
  }
</script>
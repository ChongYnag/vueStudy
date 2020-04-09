<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->

    <!-- <TplDemo/> -->

    <!-- <EventDemo/> -->
    <ComputedDemo />
    <WatchDemo />
    <ClassDemo />
    <ConditionDemo />
    <ListDemo />
    <EventDemo />
    <FormDemo />
    <ComponentDemo />

    <AdvancedUse />

  </div>
</template>

<script>
import ComputedDemo from "./components/BaseUse/ComputedDemo";
import WatchDemo from "./components/BaseUse/WatchDemo";
import ClassDemo from "./components/BaseUse/ClassDemo";
import ConditionDemo from "./components/BaseUse/ConditionDemo";
import ListDemo from "./components/BaseUse/ListDemo";
import EventDemo from "./components/BaseUse/EventDemo";
import FormDemo from "./components/BaseUse/FormDemo";
import ComponentDemo from "./components/ComponentsDemo/index";

// import HelloWorld from './components/HelloWorld.vue'

// import TplDemo from './components/BaseUse/TplDemo'

// import EventDemo from './components/BaseUse/EventDemo'

import AdvancedUse from "./components/AdvancedUse/index";

// import CartDemo from './components/Cart/index'

export default {
  name: "app",
  components: {
    ComputedDemo,
    WatchDemo,
    ClassDemo,
    ConditionDemo,
    ListDemo,
    EventDemo,
    FormDemo,
    ComponentDemo,

    AdvancedUse,
    // HelloWorld
    // EventDemo
    // ComponentDemo
    // AdvancedUse
    // CartDemo
  }
};
</script>

<style>
/* #app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
} */
</style>


<template>
  <div class="app">
    <p>day la view</p>
    <home-page />
  </div>
</template>

<script>
import { defineComponent } from "vue";
import HomePage from "./components/HomePage.vue";

export default defineComponent({
  components:{HomePage},
  data() {
    return {

    };
  }
});
</script>
<template>
    <div class="home">
        <h1>This is an Home page</h1>
        <example-card-component />
    </div>
</template>

<script lang="ts">
  import Vue from 'vue'
  import {Component} from "vue-property-decorator";

  // Components Imports:
  import ExampleCardComponent from "@/components/ExampleCardComponent.vue";

  @Component({
      components:{
          ExampleCardComponent
      }
  })
  export default class Home extends Vue{}
</script>

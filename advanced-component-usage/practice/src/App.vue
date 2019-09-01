<template>
  <div class="container">
    <div class="row">
      <div class="col-xs-12">
        <br />
        <button class="btn btn-primary" @click="selectedComponenet = 'appBlue'">Load Blue Template</button>
        <button class="btn btn-success" @click="selectedComponenet = 'appGreen'">Load Green Template</button>
        <button class="btn btn-danger" @click="selectedComponenet = 'appRed'">Load Red Template</button>
        <hr />
        <component :is="selectedComponenet">
          <p>This is the content</p>
        </component>
        <!-- <app-blue>
          <p>This is the content</p>
        </app-blue>
        <app-green>
          <p>This is the content</p>
        </app-green>
        <app-red>
          <p>This is the content</p>
        </app-red>-->
      </div>
    </div>
  </div>
</template>

<script>
import Blue from "./components/Blue.vue";
import Green from "./components/Green.vue";
import Red from "./components/Red.vue";

export default {
  data: function() {
    return {
      selectedComponenet: "appBlue"
    };
  },
  components: {
    appBlue: Blue,
    appGreen: Green,
    appRed: Red
  }
};
</script>

<style>
</style>

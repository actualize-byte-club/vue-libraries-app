<template>
  <div>
    <pie-chart :data="data"></pie-chart>

    <VueMultiselect v-model="selected" :options="options" :multiple="true">
    </VueMultiselect>

    <p>Selected v-model: {{ selected }}</p>
  </div>
</template>

<script>
import VueMultiselect from "vue-multiselect";

export default {
  components: { VueMultiselect },
  data() {
    return {
      selected: null,
      options: ["list", "of", "options", "a", "b", "c"],
      data: [
        ["Blueberry", 44],
        ["Strawberry", 23],
        ["Pineapple", 45]
      ]
    };
  }
};
</script>

<style src="vue-multiselect/dist/vue-multiselect.css"></style>

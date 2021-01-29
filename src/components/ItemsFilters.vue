<template>
  <div class="items-filters">
    <h4 v-for="item in data" :key="item.value" style="color: red">
      <span> {{ item.title }}</span>
      <p v-for="itemChild in item.items" :key="itemChild.value">
        <span> {{ itemChild.title }}</span>
        <v-checkbox :label="itemChild.content"> </v-checkbox>
        <filters-item-child :propListCheckbox="itemChild.items" />
      </p>
    </h4>
  </div>
</template>
<script>
import FiltersItemChild from "./FiltersItemChild.vue";
export default {
  name: "ItemsFilters",
  components: { FiltersItemChild },
  props: {
    data: {
      type: Array,
      required: false,
      default: () => [],
    },
  },
  data() {
    return {};
  },
};
</script>
<style lang="scss" scoped>
</style>
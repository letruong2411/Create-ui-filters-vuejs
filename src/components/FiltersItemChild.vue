<template>
  <div class="filters-item-child">
    <v-checkbox
      v-for="item in propListCheckbox"
      :key="item.value"
      :label="item.title"
      style="margin-left:20px"
    ></v-checkbox>
  </div>
</template>
<script>
export default {
  name: "FilterItemChild",
  components: {},
  props: {
    propListCheckbox: {
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
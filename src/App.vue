<template>
  <v-app>
    adsadsa
    <filters />
    <!-- 
   <div class="filters">
    <div class="">
      <v-btn
        class="ma-2"
        color="primary"
        width="195"
        height="36"
        @click="expand = !expand"
      >
        <v-icon>mdi-filter</v-icon>
        <span> haha  </span>
        <span> B </span>
      </v-btn>

      <v-expand-transition>
        <v-card v-show="expand" height="500" width="300" class="mx-auto" style="position: fixed">
          <v-checkbox v-model="model"></v-checkbox> -->

    <!-- <v-list-item>
            <v-list-item-content>
              <v-list-item-title class="title">
                {{ $t('home.content.filters.area.title') }}
              </v-list-item-title>
            </v-list-item-content>
          </v-list-item>

          <v-list-item>
            <v-list-item-title class="title">
              {{ $t('home.content.filters.area.security.title') }}
            </v-list-item-title>
          </v-list-item>

          <v-list-item-subtitle>
            <v-list-item v-for="item in items" :key="item.id">
              <v-checkbox
                v-model="model"
                color="primary"
                :value="item"
                :label="$t('home.content.filters.area.security.title')"
              ></v-checkbox>
            </v-list-item>

            <v-list-item>
              <template #default="{ active }">
                <v-list-item-action v-for="item in items" :key="item.id">
                  <v-checkbox
                    v-model="model"
                    :input-value="active"
                    color="primary"
                    :label="item.name"
                    :value="item"
                  ></v-checkbox>
                </v-list-item-action>
              </template>
            </v-list-item>
          </v-list-item-subtitle> -->
    <!-- </v-card>
      </v-expand-transition>
    </div>
  </div> -->
  </v-app>
</template>

<script>
import Filters from "./components/Filters.vue";
export default {
  name: "App",

  components: { Filters },

  data() {
    return {
      // expand: false,
      selected: [],
      allSelected: false,
      model: [],
      items: [
        {
          id: 1,
          name: "Item1",
        },
        {
          id: 2,
          name: "Item2",
        },
        {
          id: 3,
          name: "Item3",
        },
        {
          id: 4,
          name: "Item4",
        },
      ],
    };
  },
};
</script>
<style lang="scss" scoped>
.filters {
  display: flex;
  justify-content: flex-end;
  top: 57px;
  border-radius: 8px;
  padding: 16px;
}
</style>

<template>
  <div class="filters">
    <div>
      <v-btn class="ma-2" color="primary" width="195" @click="expand = !expand">
        <v-icon>mdi-filter</v-icon>
        <span> MAP表示の切り替え </span>
        <span> B </span>
      </v-btn>
      <v-expand-transition>
        <v-card
          v-show="expand"
          height="500"
          width="300"
          class="mx-auto"
          style="display: flex !important; flex-direction: column; position: fixed"
        >
          <items-filters :data="data" style="flex-grow: 1; overflow: auto;" />
        </v-card>
      </v-expand-transition>
    </div>
  </div>
</template>
<script>
import ItemsFilters from "./ItemsFilters.vue";
export default {
  name: "Filters",

  components: { ItemsFilters },
  data() {
    return {
      expand: false,
      data: [
        {
          value: "AREA_DISPLAY",
          title: "エリア表示",
          items: [
            {
              value: "SECURITY",
              title: "災害・治安",
              content: "ハザードマップ",
              checked: false,
              items: [
                {
                  value: "SECURITY_FLOOD_INFORMATION",
                  title: "洪水情報",
                  checked: false,
                },
                {
                  value: "SECURITY_SEDIMENT_DISASSTER",
                  title: "土砂災害",
                  checked: false,
                },
                {
                  value: "SECURITY_TSUNAMI",
                  title: "津波",
                  checked: false,
                },
              ],
            },
            {
              value: "INFORMATION",
              title: "土地道路基本情報",
              content: "用途地域分類",
              checked: false,
              items: [
                {
                  value: "INFORMATION_TYPE_1",
                  title: "第一種低層住居専用地域",
                  checked: false,
                },
                {
                  value: "INFORMATION_TYPE_2",
                  title: "第二種低層住居専用地域",
                  checked: false,
                },
                {
                  value: "INFORMATION_TYPE_3",
                  title: "第一種中高層居住専用地域",
                  checked: false,
                },
                {
                  value: "INFORMATION_TYPE_4",
                  title: "第二種中高層居住専用地域",
                  checked: false,
                },
                {
                  value: "INFORMATION_TYPE_5",
                  title: "第一種居住地域",
                  checked: false,
                },
                {
                  value: "INFORMATION_TYPE_6",
                  title: "第一種居住地域",
                  checked: false,
                },
                {
                  value: "INFORMATION_TYPE_7",
                  title: "第一種居住地域",
                  checked: false,
                },
                {
                  value: "INFORMATION_TYPE_8",
                  title: "第一種居住地域",
                  checked: false,
                },
                {
                  value: "INFORMATION_TYPE_9",
                  title: "第一種居住地域",
                  checked: false,
                },
                {
                  value: "INFORMATION_TYPE_10",
                  title: "第一種居住地域",
                  checked: false,
                },
                {
                  value: "INFORMATION_TYPE_11",
                  title: "第一種居住地域",
                  checked: false,
                },
                {
                  value: "INFORMATION_TYPE_12",
                  title: "第一種居住地域",
                  checked: false,
                },
              ],
            },
          ],
        },
        {
          value: "SPOT_DISPLAY",
          title: "スポット表示",
          items: [
            {
              value: "SPOT_DISPLAY_RAILWAY_STATION",
              content: "鉄道駅",
              checked: false,
            },
            {
              value: "SPOT_DISPLAY_BUS_TOP",
              content: "バス停",
              checked: false,
            },
            {
              value: "SPOT_DISPLAY_PARKING_LOT",
              content: "駐車場",
              checked: false,
            },
            {
              value: "SPOT_DISPLAY_CYCLE_SHARE_STATION",
              content: "サイクルシェアステーション ",
              checked: false,
            },
            {
              value: "SPOT_DISPLAY_SCHOOL_DEVIATIOádN_VALUE",
              content: "学校偏差値",
              checked: false,
            },
            {
              value: "SPOT_DISPLAY_SCHOOL_DEVIATIOaaN_VALUE",
              content: "学校偏差値",
              checked: false,
            },
            {
              value: "SPOT_DISPLAY_SCHOOL_DEVIATIrrrON_VALUE",
              content: "学校偏差値",
              checked: false,
            },
          ],
        },
      ],
    };
  },
};
</script>
<style lang="scss" scoped>
</style>
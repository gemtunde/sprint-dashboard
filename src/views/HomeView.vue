<template>
  <v-app id="inspire" :style="{background: $vuetify.theme.themes.dark.background}">
    <side-bar />
    <side-bar-right />
  </v-app>
</template>

<script>
import SideBar from '@/components/SideBar.vue'
import SideBarRight from '@/components/SideBarRight.vue'
import { use } from 'echarts';
import {CanvasRenderer} from "echarts/renderers";
import {PieChart} from "echarts/core";
import {
  TitleComponent,
  TooltipComponent,
  LegendComponent,
} from "echarts/components";
//import VChart, {THEME_KEY} from "vue-echarts"

use([
   PieChart,
  CanvasRenderer,
  TitleComponent,
  TooltipComponent,
  LegendComponent,
]);

  export default {
    name: 'HomePage',
    data : ()=>({
      toggle_exclusive : 1,
      orders : [
        {
          id: "P42",
          title: "Onboarding",
          state: "Delivered",
          count : 3,
          icon: "fas fa-ellipsis-h"
        } ,   
        {
          id: "P22",
          title: "User Profule",
          state: "Delivered",
          count : 13,
          icon: "fas fa-ellipsis-h"
        } ,   
        {
          id: "P56",
          title: "Landing Page",
          state: "Approved",
          count : 7,
          icon: "fas fa-ellipsis-h"
        } ,   
        {
          id: "P37",
          title: "Setting",
          state: "Approved",
          count : 9,
          icon: "fas fa-ellipsis-h"
        } ,      
      ],
      option:{
        title : {
          text: "Burnsown chart",
          left: "left"
        },
        tooltip : {
          trigger: "item",
          formatter: "{a} <br/>{b} : {c} ({d}%)"
        },

        series: [
          {
            name : "Traffic Sources",
            type: "pie",
            radius: "55%",
            center: ["45%", "50%"],
            data: [
              {value:335, name: "Direct"},
              {value:315, name: "Email"},
              {value:235, name: "Ad Networks"},
              {value:135, name: "Video Ads"},
              {value:335, name: "Direct"},
              {value:1335, name: "Search Engines"},
            ],
            emphasis:{
              itemStyle : {
                shadowBlur :10,
                shadowOffsetX: 0,
                shadowColor : "rgba(0,0,0,0)"
              }
            }
          }
        ],
      },
    }),
    components: {
        SideBar,
        SideBarRight,
       // VChart,
    },
    provide : {
     // [THEME_KEY] : "green"
    }
  }
</script>
<style scoped>
  .space {
    margin-left: -100px;
    margin-right: -100px;
  }
</style>
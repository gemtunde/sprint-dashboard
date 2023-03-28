<template>
  <v-app id="inspire" :style="{background: $vuetify.theme.themes.dark.background}">
    <side-bar />
    <side-bar-right />  
     <v-container>
      <v-toolbar color="rgba(0,0,0,0)" flat class="mt-n4">
        <v-btn-toggle v-model="toggle_exclusive" tile group color="#49D9A0">
            <v-btn text>
                <v-icon> fas fa-arrow-left</v-icon>
            </v-btn>
            <v-btn text>
                <v-icon> fas fa-arrow-right</v-icon>
            </v-btn>
        </v-btn-toggle>
        <v-spacer></v-spacer>
        <v-btn color="#49D9A0" rounded dark>
                 Finish Sprint
              </v-btn>
      </v-toolbar>
      <v-toolbar color="rgba(0,0,0,0)" flat class="mt-n5">
          <v-toolbar-title> Sprint Overview</v-toolbar-title>
          <v-btn color="#49D9A0" text class="ml-5"> Last Sprint</v-btn>
      </v-toolbar>
      <v-item-group mandatory class="mt-n4">
          <v-container>
              <v-row justify="center" class="space">
                  <v-col cols="12" md="2">
                      <v-item v-slot="{active, toggle}">
                          <v-card :color= " active ? '#40D9A0' : 'white' "
                            class="d-flex align-center rounded-xl"
                            dark
                            height="200"
                            @click="toggle"
                          >
                            <v-row>
                              <v-col cols="12" sm="12">
                                <v-list-item three-line class="mt-10">
                                    <v-list-item-content>
                                       <div class="mb-4">
                                          <v-icon x-large :color= "active ? 'white' : '#40D9A0' ">
                                            fas fa-chart-bar
                                          </v-icon>
                                       </div>
                                         <v-list-item-subtitle :class= "active ? 'white--text' : 'black--text'"> Team Velocity</v-list-item-subtitle>
                                         <v-list-item-title class="headline mb-1" :class= "active ? 'white--text' : 'black--text'"></v-list-item-title>
                                          <strong :class= "active ? 'white--text' : 'black--text'">58</strong>
                                        </v-list-item-content>
                                </v-list-item>

                              </v-col>
                            </v-row>
                          </v-card>
                      </v-item>
                  </v-col>
                    <v-col cols="12" md="2">
                        <v-item v-slot="{ active, toggle }">
                            <v-card :color= "active ? '#40D9A0' : 'white'"
                              class="d-flex align-center rounded-xl"
                              dark
                              height="200"
                              @click="toggle"
                            >
                              <v-row>
                                <v-col cols="12" sm="12">
                                  <v-list-item three-line class="mt-10">
                                      <v-list-item-content>
                                         <div class="mb-4">
                                            <v-icon x-large :color= "active ? 'white' : '#40D9A0'">
                                              fas fa-user
                                            </v-icon>
                                         </div>
                                           <v-list-item-subtitle :class= "active ? 'white--text' : 'black--text'"> Team Members</v-list-item-subtitle>
                                           <v-list-item-title class="headline mb-1" :class= "active ? 'white--text' : 'black--text'"></v-list-item-title>
                                            <strong :class= "active ? 'white--text' : 'black--text'">32</strong>
                                          </v-list-item-content>
                                  </v-list-item>

                                </v-col>
                              </v-row>
                            </v-card>
                        </v-item>
                    </v-col>
                      <v-col cols="12" md="2">
                          <v-item v-slot="{ active, toggle }">
                              <v-card :color= "active ? '#40D9A0' : 'white'"
                                class="d-flex align-center rounded-xl"
                                dark
                                height="200"
                                @click="toggle"
                              >
                                <v-row>
                                  <v-col cols="12" sm="12">
                                    <v-list-item three-line class="mt-10">
                                        <v-list-item-content>
                                           <div class="mb-4">
                                              <v-icon x-large :color= "active ? 'white' : '#40D9A0'">
                                                fas fa-suitcase
                                              </v-icon>
                                           </div>
                                             <v-list-item-subtitle :class= "active ? 'white--text' : 'black--text'"> Tasks Delivered</v-list-item-subtitle>
                                             <v-list-item-title class="headline mb-1" :class= "active ? 'white--text' : 'black--text'"></v-list-item-title>
                                              <strong :class= "active ? 'white--text' : 'black--text'">19</strong>
                                            </v-list-item-content>
                                    </v-list-item>

                                  </v-col>
                                </v-row>
                              </v-card>
                          </v-item>
                      </v-col>
                        <v-col cols="12" md="2">
                          <v-item v-slot="{ active, toggle }">
                              <v-card :color= "active ? '#40D9A0' : 'white'"
                                class="d-flex align-center rounded-xl"
                                dark
                                height="200"
                                @click="toggle"
                              >
                                <v-row>
                                  <v-col cols="12" sm="12">
                                    <v-list-item three-line class="mt-10">
                                        <v-list-item-content>
                                           <div class="mb-4">
                                              <v-icon x-large :color= "active ? 'white' : '#40D9A0'">
                                                fas fa-search
                                              </v-icon>
                                           </div>
                                             <v-list-item-subtitle :class= "active ? 'white--text' : 'black--text'"> Spikes Delivered</v-list-item-subtitle>
                                             <v-list-item-title class="headline mb-1" :class= "active ? 'white--text' : 'black--text'"></v-list-item-title>
                                              <strong :class= "active ? 'white--text' : 'black--text'">87</strong>
                                            </v-list-item-content>
                                    </v-list-item>

                                  </v-col>
                                </v-row>
                              </v-card>
                          </v-item>
                      </v-col>
                        <v-col cols="12" md="2">
                          <v-item v-slot="{ active, toggle }">
                              <v-card :color= "active ? '#40D9A0' : 'white'"
                                class="d-flex align-center rounded-xl"
                                dark
                                height="200"
                                @click="toggle"
                              >
                                <v-row>
                                  <v-col cols="12" sm="12">
                                    <v-list-item three-line class="mt-10">
                                        <v-list-item-content>
                                           <div class="mb-4">
                                              <v-icon x-large :color= "active ? 'white' : '#40D9A0'">
                                                fas fa-globe-africa
                                              </v-icon>
                                           </div>
                                             <v-list-item-subtitle :class= "active ? 'white--text' : 'black--text'"> News Event</v-list-item-subtitle>
                                             <v-list-item-title class="headline mb-1" :class= "active ? 'white--text' : 'black--text'"></v-list-item-title>
                                              <strong :class= "active ? 'white--text' : 'black--text'">102</strong>
                                            </v-list-item-content>
                                    </v-list-item>

                                  </v-col>
                                </v-row>
                              </v-card>
                          </v-item>
                      </v-col>
              </v-row>              
          </v-container>          
      </v-item-group>
      <v-row class="mt-n6">
          <v-col cols="12" sm="7">
              <v-chart class="chart mt-2" :option="option"/>
          </v-col>
          <v-col cols="12" md="5" sm="12">
              <v-toolbar color="rgba(0,0,0,0)" flat class="mt-n2">
                  <v-toolbar-title>Sprint Stories</v-toolbar-title>
                  <v-spacer></v-spacer>
                  <v-btn rounded small> See All</v-btn>
              </v-toolbar>
              <v-simple-table class="grey ligthen-3">
                  <template v-slot:default>
                    <tbody> 
                      <tr v-for="item in orders" :key="item.name">
                        <td>{{ item.id }}</td>
                        <td>{{ item.title }}</td>
                        <td>{{ item.state }}</td>
                        <td>{{ item.count }}</td>
                        <td> <v-icon small> {{ item.icon }} </v-icon></td>
                      </tr>
                    </tbody>
                  </template>
              </v-simple-table>
          </v-col>
      </v-row>
      <v-toolbar color="rgba(0,0,0,0)" flat class="mt-n8">
          <v-toolbar-title> Team Members</v-toolbar-title>
          <v-spacer></v-spacer>
          <v-btn rounded small> Add Member</v-btn>          
      </v-toolbar>
      <v-card class="rounded-lg">
        <v-row>
            <v-col cols="12" sm="3">
                <v-list subheader two-line>
                    <v-list-item>
                        <v-badge bordered bottom color="#49D9A0" dot offset-x="28" offset-y="22">
                            <v-list-item-avatar>
                                <v-avatar size="40">
                                    <v-img src="https://avatars.githubusercontent.com/u/52404803?v=4"></v-img>
                                </v-avatar>
                            </v-list-item-avatar>
                        </v-badge>
                        <v-list-item-content>
                          <v-list-item-title>gemtunde</v-list-item-title>
                          <v-list-item-subtitle>Frontend Engr</v-list-item-subtitle>
                        </v-list-item-content>
                    </v-list-item>
                </v-list>
            </v-col>
            <v-col cols="12" sm="3">
                <v-list subheader two-line>
                    <v-list-item>
                        <v-badge bordered bottom color="#49D9A0" dot offset-x="28" offset-y="22">
                            <v-list-item-avatar>
                                <v-avatar size="40">
                                    <v-img src="https://avatars.githubusercontent.com/u/52404803?v=4"></v-img>
                                </v-avatar>
                            </v-list-item-avatar>
                        </v-badge>
                        <v-list-item-content>
                          <v-list-item-title>gemtunde</v-list-item-title>
                          <v-list-item-subtitle>Frontend Engr</v-list-item-subtitle>
                        </v-list-item-content>
                    </v-list-item>
                </v-list>
            </v-col>
            <v-col cols="12" sm="3">
                <v-list subheader two-line>
                    <v-list-item>
                        <v-badge bordered bottom color="#49D9A0" dot offset-x="28" offset-y="22">
                            <v-list-item-avatar>
                                <v-avatar size="40">
                                    <v-img src="https://avatars.githubusercontent.com/u/52404803?v=4"></v-img>
                                </v-avatar>
                            </v-list-item-avatar>
                        </v-badge>
                        <v-list-item-content>
                          <v-list-item-title>gemtunde</v-list-item-title>
                          <v-list-item-subtitle>Frontend Engr</v-list-item-subtitle>
                        </v-list-item-content>
                    </v-list-item>
                </v-list>
            </v-col>
            <v-col cols="12" sm="3">
                <v-list subheader two-line>
                    <v-list-item>
                        <v-badge bordered bottom color="#49D9A0" dot offset-x="28" offset-y="22">
                            <v-list-item-avatar>
                                <v-avatar size="40">
                                    <v-img src="https://avatars.githubusercontent.com/u/52404803?v=4"></v-img>
                                </v-avatar>
                            </v-list-item-avatar>
                        </v-badge>
                        <v-list-item-content>
                          <v-list-item-title>gemtunde</v-list-item-title>
                          <v-list-item-subtitle>Frontend Engr</v-list-item-subtitle>
                        </v-list-item-content>
                    </v-list-item>
                </v-list>
            </v-col>
        </v-row>
      </v-card>
    </v-container>
  </v-app>
</template>

<script>
import SideBar from '@/components/SideBar.vue'
import SideBarRight from '@/components/SideBarRight.vue'
import { use } from 'echarts/core';
//import {CanvasRenderer} from "charts/renderers";
import {PieChart} from "echarts/charts";
import {
  TitleComponent,
  TooltipComponent,
  LegendComponent,
} from "echarts/components";
import VChart, {THEME_KEY} from "vue-echarts"

use([
   PieChart,
 // CanvasRenderer,
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
        VChart,
    },
    provide : {
      [THEME_KEY] : "green"
    }
  }
</script>
<style scoped>
  .space {
    margin-left: -100px;
    margin-right: -100px;
  }
</style>
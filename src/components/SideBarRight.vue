<template>
   <v-navigation-drawer app color="white" right width="290">
        <v-toolbar color="rgba(0,0,0,0)" flat>
            <v-toolbar-title>Sprint</v-toolbar-title>
            <v-spacer></v-spacer>
            <v-btn rounded small>
                See All
            </v-btn>
        </v-toolbar>
        <v-list subheader two-line class="mt-n4">
            <v-list-item v-for="file in files" :key="file.title">
                <v-list-item-avatar>
                    <v-icon :class="file.color" dark v-text="file.icon" snall></v-icon>
                </v-list-item-avatar>
                <v-list-item-content>
                    <v-list-item-title v-text="file.title"></v-list-item-title>
                    <v-list-item-subtitle v-text="file.subtitle"></v-list-item-subtitle>
                </v-list-item-content>
                <v-list-item-action>
                    <v-btn icon>
                        <v-icon color="grey ligthen-1" small> fas fa-ellipsis-h</v-icon>
                    </v-btn>
                </v-list-item-action>
            </v-list-item>
        </v-list>
        <v-toolbar color="rgba(0,0,0,0)" flat class="mt-n6">
            <v-toolbar-title>Project Statistics</v-toolbar-title>
        </v-toolbar>
        <v-card class="mx-2 mt-4 mb-4 rounded-l-xl pb-1" flat color="#EEEEEE">
            <v-row>
                <v-col cols="12" sm="5">
                    <v-list-item two-line class="mt-n4">
                        <v-list-item-content>
                            <v-list-item-title> Project</v-list-item-title>
                            <v-list-item-subtitle> Progress</v-list-item-subtitle>
                        </v-list-item-content>
                    </v-list-item>
                </v-col>
                <v-col cols="12" sm="4">
                    <v-progress-circular :size="50" :width="3" :value="75" color="teal" class="ml-n5 mt-n1">
                        75
                    </v-progress-circular>
                </v-col>
            </v-row>
        </v-card>
        <v-card class="mx-2 mt-4 mb-4 rounded-l-xl pb-1" flat color="#EEEEEE">
            <v-row>
                <v-col cols="12" sm="5">
                    <v-list-item two-line class="mt-n4">
                        <v-list-item-content>
                            <v-list-item-title>Business</v-list-item-title>
                            <v-list-item-subtitle> Business</v-list-item-subtitle>
                        </v-list-item-content>
                    </v-list-item>
                </v-col>
                <v-col cols="12" sm="4">
                    <v-progress-circular :size="50" :width="3" :value="30" color="orange" class="ml-n5 mt-n1">
                        30
                    </v-progress-circular>
                </v-col>
            </v-row>
        </v-card>
        <v-card class="mx-2  mt-4 mb-4 rounded-l-xl pb-1" flat color="#EEEEEE">
            <v-row>
                <v-col cols="12" sm="5">
                    <v-list-item two-line class="mt-n4">
                        <v-list-item-content>
                            <v-list-item-title>Percentage</v-list-item-title>
                            <v-list-item-subtitle> Percentage</v-list-item-subtitle>
                        </v-list-item-content>
                    </v-list-item>
                </v-col>
                <v-col cols="12" sm="4">
                    <v-progress-circular :size="50" :width="3" :value="45" color="red" class="ml-n5 mt-n1">
                        45
                    </v-progress-circular>
                </v-col>
            </v-row>
        </v-card>
        <div class="mt-2 mx-2">
            <v-btn rounded small block>
                Project Details
            </v-btn>
        </div>
   </v-navigation-drawer>
</template>
<script>
export default {
    data: ()=> ({
        files: [
            {
                color:'green',
                icon: 'fas fa-mobile',
                subtitle: 'Design',
                title: 'Mobile Onboarding',
            },
            {
                color:'red',
                icon: 'fas fa-address-card',
                subtitle: 'Development',
                title: 'Adding Item',
            },
            {
                color:'orange',
                icon: 'fas fa-user-child',
                subtitle: 'Design',
                title: 'Admin Panel',
            },
            {
                color:'purple',
                icon: 'fas fa-drafting-compass',
                subtitle: 'Design & Development',
                title: 'Mobile MVP',
            },
            {
                color:'blue',
                icon: 'fas fa-file-code',
                subtitle: 'Research',
                title: 'QR Scan',
            },
        ]
    })
}
</script>
<style></style>
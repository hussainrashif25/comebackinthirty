<template>
  <v-app>
    <v-content>
      <div class="blue darken-3">
      <v-container style="height: 500px">
        <v-row justify="center" align="center">
          <v-card-title class="white--text">
            comebackinthirty!
          </v-card-title>
        </v-row>
          <v-row justify="center" align="center">
          <p class="white--text">comebackinthirty takes a different approach to task management, by having you comeback
            <br>every thirty minutes to log what you have done. Simply log what you have done and come back
            <br>in thirty minutes to log your new task or the same one. </p>
          </v-row>
        </v-row>
        <v-row justify="center" align="end">
            <clock/>
        </v-row>
      </v-container>
      </div>
      <v-divider></v-divider>
      
      <v-container class="scroll-y" fluid="">

          <v-btn
            bottom=""
            right=""
            v-scroll="onScroll"
            v-show="fab"
            dark=""
            fab
            fixed
            color="blue darken-3"
            @click="toTop"
          >   
            <v-icon>midi-plus</v-icon>
          </v-btn>
          <v-btn
            style="bottom: 90px"
            bottom=""
            right=""
            v-scroll="onScroll"
            v-show="fab"
            dark=""
            fab
            fixed
            color="blue darken-3"
          >
            <v-icon>mdi-pencil</v-icon>
          </v-btn>

        <v-row>
          <v-col></v-col>
          <v-col>
            <timeline
            v-for="time in times"
            v-bind:key="time.id"
            v-bind:title="time.title"
            v-bind:id="time.id"
            ></timeline>
          </v-col>
          <v-col></v-col>
        </v-row>
      </v-container>
    </v-content>

    <v-footer>
    </v-footer>
  </v-app>
</template>

<script>
import timeline from './components/timeline';
import clock from './components/clock';

export default {
  name: 'App',
  components: {
    timeline,
    clock,
  },
  data: () => ({
    fab: false,

    times: [
      {
        id: 0,
        title : '1:00 AM-1:30 AM',
        msg:'',
        clr: null,
      },
      {
        id: 1,
        title : '1:30 AM-2:00 AM',
        msg:'',
        clr: null,
      },
      {
        id: 2,
        title : '2:00 AM-2:30 AM',
        msg:'',
        clr: null,
      },
      {
        id: 3,
        title : '2:30 AM-3:00 AM',
        msg:'',
        clr: null,
      },
      {
        id: 4,
        title : '3:00 AM-3:30 AM',
        msg:'',
        clr: null,
      },
      {
        id: 5,
        title : '3:30 AM-4:00 AM',
        msg:'',
        clr: null,
      },
      {
        id: 6,
        title : '4:00 AM-4:30 AM',
        msg:'',
        clr: null,
      },
      {
        id: 7,
        title : '4:30 AM-5:00 AM',
        msg:'',
        clr: null,
      },
      {
        id: 8,
        title : '5:00 AM-5:30 AM',
        msg:'',
        clr: null,
      },
      {
        id: 9,
        title : '5:30 AM-6:00 AM',
        msg:'',
        clr: null,
      },
      {
        id: 10,
        title : '6:00 AM-6:30 AM',
        msg:'',
        clr: null,
      },
      {
        id: 11,
        title : '6:30 AM-7:00 AM',
        msg:'',
        clr: null,
      },
      {
        id: 12,
        title : '7:00 AM-7:30 AM',
        msg:'',
        clr: null,
      },
      {
        id: 13,
        title : '7:30 AM-8:00 AM',
        msg:'',
        clr: null,
      },
      {
        id: 14,
        title : '8:00 AM-8:30 AM',
        msg:'',
        clr: null,
      },
      {
        id: 15,
        title : '8:30 AM-9:00 AM',
        msg:'',
        clr: null,
      },
      {
        id: 16,
        title : '9:00 AM-9:30 AM',
        msg:'',
        clr: null,
      },
      {
        id: 17,
        title : '9:30 AM-10:00 AM',
        msg:'',
        clr: null,
      },
      {
        id: 18,
        title : '10:00 AM-10:30 AM',
        msg:'',
        clr: null,
      },
      {
        id: 19,
        title : '10:30 AM-11:00 AM',
        msg:'',
        clr: null,
      },
      {
        id: 20,
        title : '11:00 AM-11:30 AM',
        msg:'',
        clr: null,
      },
      {
        id: 21,
        title : '11:30 AM-12:00 PM',
        msg:'',
        clr: null,
      },
      {
        id: 22,
        title : '12:00 PM-12:30 PM ',
        msg:'',
        clr: null,
      },
      {
        id: 23,
        title : '12:30 PM-1:00 PM',
        msg:'',
        clr: null,
      },
      {
        id: 24,
        title : '1:00 PM-1:30 PM',
        msg:'',
        clr: null,
      },
      {
        id: 25,
        title : '1:30 PM-2:00 PM',
        msg:'',
        clr: null,
      },
      {
        id: 26,
        title : '2:00 PM-2:30 PM',
        msg:'',
        clr: null,
      },
      {
        id: 27,
        title : '2:30 PM-3:00 PM',
        msg:'',
        clr: null,
      },
      {
        id: 28,
        title : '3:00 PM-3:30 PM',
        msg:'',
        clr: null,
      },
      {
        id: 29,
        title : '3:30 PM-4:00 PM',
        msg:'',
        clr: null,
      },
      {
        id: 30,
        title : '4:00 PM-4:30 PM',
        msg:'',
        clr: null,
      },
      {
        id: 31,
        title : '4:30 PM-5:00 PM',
        msg:'',
        clr: null,
      },
      {
        id: 32,
        title : '5:00 PM-5:30 PM',
        msg:'',
        clr: null,
      },
      {
        id: 33,
        title : '5:30 PM-6:00 PM',
        msg:'',
        clr: null,
      },
      {
        id: 34,
        title : '6:00 PM-6:30 PM',
        msg:'',
        clr: null,
      },
      {
        id: 35,
        title : '6:30 PM-7:00 PM',
        msg:'',
        clr: null,
      },
      {
        id: 36,
        title : '7:00 PM-7:30 PM',
        msg:'',
        clr: null,
      },
      {
        id: 37,
        title : '7:30 PM-8:00 PM',
        msg:'',
        clr: null,
      },
      {
        id: 38,
        title : '8:00 PM-8:30 PM',
        msg:'',
        clr: null,
      },
      {
        id: 39,
        title : '8:30 PM-9:00 PM',
        msg:'',
        clr: null,
      },
      {
        id: 40,
        title : '9:00 PM-9:30 PM',
        msg:'',
        clr: null,
      },
      {
        id: 41,
        title : '9:30 PM-10:00 PM',
        msg:'',
        clr: null,
      },
      {
        id: 42,
        title : '10:00 PM-10:30 PM',
        msg:'',
        clr: null,
      },
      {
        id: 43,
        title : '10:30 PM-11:00 PM',
        msg:'',
        clr: null,
      },
      {
        id: 44,
        title : '11:00 PM-11:30 PM',
        msg:'',
        clr: null,
      },
      {
        id: 45,
        title : '11:30 PM-12:00 AM',
        msg:'',
        clr: null,
      },
      {
        id: 46,
        title : '12:00 PM-12:30 AM',
        msg:'',
        clr: null,
      },
      {
        id: 47,
        title : '12:30 PM-1:00 AM',
        msg:'',
        clr: null,
      },
    ]
    //
  }),

  methods: {
    onScroll(e) {
            if (typeof window === 'undefined') return
            const top = window.pageYOffset || e.target.scrollTop || 0
            this.fab = top > 20
        },
  }
};
</script>

<style>
  .fab-container {
    position: fixed;
    bottom: 0;
    right: 0;
  }
</style>

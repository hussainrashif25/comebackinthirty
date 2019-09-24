<template>
  <v-app>
    <v-content>
      <timeline
      v-for="time in times"
      v-bind:key="time.id"
      v-bind:title="time.title"
      v-bind:id="time.id"
      ></timeline>
    </v-content>
  </v-app>
</template>

<script>
import timeline from './components/timeline';

export default {
  name: 'App',
  components: {
    timeline,
  },
  data: () => ({
    times: [
      {
        id: 1,
        title : '1:00 AM-1:30 AM',
        msg:'',
        clr: null,
      },
      {
        id: 2,
        title : '1:30 AM-2:00 AM',
        msg:'',
        clr: null,
      },
      {
        id: 3,
        title : '2:00 AM-2:30 AM',
        msg:'',
        clr: null,
      },
      {
        id: 4,
        title : '2:30 AM-3:00 AM',
        msg:'',
        clr: null,
      },
      {
        id: 5,
        title : '3:00 AM-3:30 AM',
        msg:'',
        clr: null,
      },
      {
        id: 6,
        title : '3:30 AM-4:00 AM',
        msg:'',
        clr: null,
      },
      {
        id: 7,
        title : '4:00 AM-4:30 AM',
        msg:'',
        clr: null,
      },
      {
        id: 8,
        title : '4:30 AM-5:00 AM',
        msg:'',
        clr: null,
      },
      {
        id: 9,
        title : '5:00 AM-5:30 AM',
        msg:'',
        clr: null,
      },
      {
        id: 10,
        title : '5:30 AM-6:00 AM',
        msg:'',
        clr: null,
      },
      {
        id: 11,
        title : '6:00 AM-6:30 AM',
        msg:'',
        clr: null,
      },
      {
        id: 12,
        title : '6:30 AM-7:00 AM',
        msg:'',
        clr: null,
      },
      {
        id: 13,
        title : '7:00 AM-7:30 AM',
        msg:'',
        clr: null,
      },
      {
        id: 14,
        title : '7:30 AM-8:00 AM',
        msg:'',
        clr: null,
      },
      {
        id: 15,
        title : '8:00 AM-8:30 AM',
        msg:'',
        clr: null,
      },
      {
        id: 16,
        title : '8:30 AM-9:00 AM',
        msg:'',
        clr: null,
      },
      {
        id: 17,
        title : '9:00 AM-9:30 AM',
        msg:'',
        clr: null,
      },
      {
        id: 18,
        title : '9:30 AM-10:00 AM',
        msg:'',
        clr: null,
      },
      {
        id: 19,
        title : '10:00 AM-10:30 AM',
        msg:'',
        clr: null,
      },
      {
        id: 20,
        title : '10:30 AM-11:00 AM',
        msg:'',
        clr: null,
      },
      {
        id: 21,
        title : '11:00 AM-11:30 AM',
        msg:'',
        clr: null,
      },
      {
        id: 22,
        title : '11:30 AM-12:00 PM',
        msg:'',
        clr: null,
      },
      {
        id: 23,
        title : '12:00 PM-12:30 PM ',
        msg:'',
        clr: null,
      },
      {
        id: 24,
        title : '12:30 PM-1:00 PM',
        msg:'',
        clr: null,
      },
      {
        id: 25,
        title : '1:00 PM-1:30 PM',
        msg:'',
        clr: null,
      },
      {
        id: 26,
        title : '1:30 PM-2:00 PM',
        msg:'',
        clr: null,
      },
      {
        id: 27,
        title : '2:00 PM-2:30 PM',
        msg:'',
        clr: null,
      },
      {
        id: 28,
        title : '2:30 PM-3:00 PM',
        msg:'',
        clr: null,
      },
      {
        id: 29,
        title : '3:00 PM-3:30 PM',
        msg:'',
        clr: null,
      },
      {
        id: 30,
        title : '3:30 PM-4:00 PM',
        msg:'',
        clr: null,
      },
      {
        id: 31,
        title : '4:00 PM-4:30 PM',
        msg:'',
        clr: null,
      },
      {
        id: 32,
        title : '4:30 PM-5:00 PM',
        msg:'',
        clr: null,
      },
      {
        id: 33,
        title : '5:00 PM-5:30 PM',
        msg:'',
        clr: null,
      },
      {
        id: 34,
        title : '5:30 PM-6:00 PM',
        msg:'',
        clr: null,
      },
      {
        id: 35,
        title : '6:00 PM-6:30 PM',
        msg:'',
        clr: null,
      },
      {
        id: 36,
        title : '6:30 PM-7:00 PM',
        msg:'',
        clr: null,
      },
      {
        id: 37,
        title : '7:00 PM-7:30 PM',
        msg:'',
        clr: null,
      },
      {
        id: 38,
        title : '7:30 PM-8:00 PM',
        msg:'',
        clr: null,
      },
      {
        id: 39,
        title : '8:00 PM-8:30 PM',
        msg:'',
        clr: null,
      },
      {
        id: 40,
        title : '8:30 PM-9:00 PM',
        msg:'',
        clr: null,
      },
      {
        id: 41,
        title : '9:00 PM-9:30 PM',
        msg:'',
        clr: null,
      },
      {
        id: 42,
        title : '9:30 PM-10:00 PM',
        msg:'',
        clr: null,
      },
      {
        id: 43,
        title : '10:00 PM-10:30 PM',
        msg:'',
        clr: null,
      },
      {
        id: 44,
        title : '10:30 PM-11:00 PM',
        msg:'',
        clr: null,
      },
      {
        id: 45,
        title : '11:00 PM-11:30 PM',
        msg:'',
        clr: null,
      },
      {
        id: 46,
        title : '11:30 PM-12:00 AM',
        msg:'',
        clr: null,
      },
      {
        id: 47,
        title : '12:00 PM-12:30 AM',
        msg:'',
        clr: null,
      },
      {
        id: 48,
        title : '12:30 PM-1:00 AM',
        msg:'',
        clr: null,
      },
    ]
    //
  }),
};
</script>

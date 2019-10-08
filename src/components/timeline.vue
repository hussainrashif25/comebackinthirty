<template>
    <v-timeline align-top dense>
        <v-timeline-item large fill-dot="">
            <v-card>
                <v-card-title><span>{{ title }}</span><v-spacer></v-spacer><v-btn
                            depressed
                            @click="delevents(id)"
                            >
                            clear
                            </v-btn></v-card-title>
                <v-expansion-panels>
                    <v-expansion-panel>
                        <v-expansion-panel-header v-slot="{open}">
                            <v-row no-gutters>
                                <v-col cols="8" class="text--secondary">
                                        <span
                                        v-if="open"
                                        key="0"
                                        >
                                        </span>
                                        <span
                                        v-else
                                        key="1"
                                        >
                                        {{events[id].msg}}
                                        </span>
                                </v-col>
                            </v-row>
                        </v-expansion-panel-header>
                        <v-expansion-panel-content>
                            <v-text-field
                            placeholder="Type event and press enter!"
                            v-model="input"
                            flat
                            hide-details=""
                            @keydown.enter="comment(id)"
                            ></v-text-field>
                        </v-expansion-panel-content>
                    </v-expansion-panel>
                </v-expansion-panels>
            </v-card>
        </v-timeline-item>
    </v-timeline>
</template>

<script>
export default {
  props: ['title', 'id'],

  data: () => ({
    events: [
      {
        id: 0,
        msg: '',
        clr: null
      },
      {
        id: 1,
        msg: '',
        clr: null
      },
      {
        id: 2,
        msg: '',
        clr: null
      },
      {
        id: 3,
        msg: '',
        clr: null
      },
      {
        id: 4,
        msg: '',
        clr: null
      },
      {
        id: 5,
        msg: '',
        clr: null
      },
      {
        id: 6,
        msg: '',
        clr: null
      },
      {
        id: 7,
        msg: '',
        clr: null
      },
      {
        id: 8,
        msg: '',
        clr: null
      },
      {
        id: 9,
        msg: '',
        clr: null
      },
      {
        id: 10,
        msg: '',
        clr: null
      },
      {
        id: 11,
        msg: '',
        clr: null
      },
      {
        id: 12,
        msg: '',
        clr: null
      },
      {
        id: 13,
        msg: '',
        clr: null
      },
      {
        id: 14,
        msg: '',
        clr: null
      },
      {
        id: 15,
        msg: '',
        clr: null
      },
      {
        id: 16,
        msg: '',
        clr: null
      },
      {
        id: 17,
        msg: '',
        clr: null
      },
      {
        id: 18,
        msg: '',
        clr: null
      },
      {
        id: 19,
        msg: '',
        clr: null
      },
      {
        id: 20,
        msg: '',
        clr: null
      },
      {
        id: 21,
        msg: '',
        clr: null
      },
      {
        id: 22,
        msg: '',
        clr: null
      },
      {
        id: 23,
        msg: '',
        clr: null
      },
      {
        id: 24,
        msg: '',
        clr: null
      },
      {
        id: 25,
        msg: '',
        clr: null
      },
      {
        id: 26,
        msg: '',
        clr: null
      },
      {
        id: 27,
        msg: '',
        clr: null
      },
      {
        id: 28,
        msg: '',
        clr: null
      },
      {
        id: 29,
        msg: '',
        clr: null
      },
      {
        id: 30,
        msg: '',
        clr: null
      },
      {
        id: 31,
        msg: '',
        clr: null
      },
      {
        id: 32,
        msg: '',
        clr: null
      },
      {
        id: 33,
        msg: '',
        clr: null
      },
      {
        id: 34,
        msg: '',
        clr: null
      },
      {
        id: 35,
        msg: '',
        clr: null
      },
      {
        id: 36,
        msg: '',
        clr: null
      },
      {
        id: 37,
        msg: '',
        clr: null
      },
      {
        id: 38,
        msg: '',
        clr: null
      },
      {
        id: 39,
        msg: '',
        clr: null
      },
      {
        id: 40,
        msg: '',
        clr: null
      },
      {
        id: 41,
        msg: '',
        clr: null
      },
      {
        id: 42,
        msg: '',
        clr: null
      },
      {
        id: 43,
        msg: '',
        clr: null
      },
      {
        id: 44,
        msg: '',
        clr: null
      },
      {
        id: 45,
        msg: '',
        clr: null
      },
      {
        id: 46,
        msg: '',
        clr: null
      },
      {
        id: 47,
        msg: '',
        clr: null
      }
    ],
    input: null,
    deep: true
  }),

  mounted () {
    if (localStorage.getItem('events')) {
      try {
        this.events = JSON.parse(localStorage.getItem('events'))
      } catch (e) {
        localStorage.removeItem('events')
      }
    }
  },

  methods: {

    comment (n) {
      if (!this.input) {
        return
      }

      localStorage.setItem('events', JSON.stringify(this.events))

      var change = JSON.parse(localStorage.getItem('events'))

      change[n].msg = this.input
      change[n].id = this.id
      /* change.splice(n, 0,{
            id: this.id,
            msg: this.input,
        }); */

      localStorage.setItem('events', JSON.stringify(change))

      this.input = null
      location.reload(true)
    },

    delevents (x) {
      localStorage.setItem('events', JSON.stringify(this.events))

      var change = JSON.parse(localStorage.getItem('events'))

      change[x].msg = ''
      change[x].id = this.id

      localStorage.setItem('events', JSON.stringify(change))
      location.reload(true)
    }

  }

}
</script>

<style>

</style>

<template>
    <v-timeline align-top dense>
        <v-timeline-item>
            <v-card>
                <v-card-title><span>{{ title }}</span></v-card-title>
                <v-expansion-panels>
                    <v-expansion-panel>
                        <v-expansion-panel-header v-slot="{open}">
                            <v-row no-gutters>
                                <v-col>edit</v-col>
                                <v-col cols="8" class="text--secondary">
                                    <v-fade-transistion leave-absolute>
                                        <span
                                        v-if="open"
                                        key="0"
                                        >
                                        </span>
                                        <span
                                        v-else
                                        key="1"
                                        >
                                        {{input}}
                                        </span>
                                    </v-fade-transistion>
                                </v-col>
                            </v-row>
                        </v-expansion-panel-header>
                        <v-expansion-panel-content>
                            <v-text-field
                            v-model="input"
                            flat
                            hide-details=""
                            @keydown.enter="comment"
                            ></v-text-field>
                            <v-btn
                            depressed
                            @click="comment"
                            >
                            save
                            </v-btn>
                        </v-expansion-panel-content>
                    </v-expansion-panel>
                </v-expansion-panels>
            </v-card>
        </v-timeline-item>
    </v-timeline>
</template>

<script>
export default {
    props: ['title'],

    data: () => ({
        events: [],
        input: null,
    }),

    mounted () {
        if (localStorage.getItem('events')) {
            try {
                this.events = JSON.parse(localStorage.getItem('events'));
            } catch(e) {
                localStorage.removeItem('events');
            }
        }
    },

    methods: {
    
    comment() {

        if (!this.input) {
        return;
        }
          
        this.events.push({
            text: this.input,
        });
        
        this.saveevents();

        this.input = null;
    },
    
    saveevents() {
      const parsed = JSON.stringify(this.events);
      localStorage.setItem('events', parsed);
    },

    delevents(x) {
      this.events.splice(x, 1);
      this.saveevents();
    }

  },



}
</script>

<style>

</style>
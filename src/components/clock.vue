<template>

      <h1 class="white--text ma-2 pa-2">{{clock}}</h1>

</template>

<script>
import moment from 'moment'
export default {
  data: () => ({
    clock: ''
  }),

  created () {
    setInterval(() => {
      this.clock = moment().format('MMMM Do YYYY, h:mm:ss a')
    }, 1000)
  }

}

</script>

<style>

</style>

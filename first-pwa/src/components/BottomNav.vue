<template>
      <q-tabs v-model="tab"
              indicator-color="transparent"
              dense
              active-color="white"
              class="bg-teal text-grey-5 shadow-2"
              align="justify"
              :breakpoint="0">
        <q-route-tab name="about" icon="mail" label="Mails" to="/"/>
        <q-route-tab name="home" icon="alarm" label="Alarms" to="/about" />
        <q-route-tab name="movies" icon="movie" label="Movies" to="/about" />
      </q-tabs>
</template>

<script>
import { ref } from 'vue'
export default {
  setup () {
    return {
      tab: ref('about')
    }
  }
}
</script>

<template>
  <div>{{ name }}</div>
</template>

<script>
import { computed } from 'vue'
import { useStore } from 'vuex'

export default {
  name: 'Dashboard',
  setup () {
    const store = useStore()

    return {
      // dashboard name getter in computed function
      setUser: () => store.commit('user/setUser'),
      name: computed(() => store.state.dashboard.name)
    }
  }
}
</script>

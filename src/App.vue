<template>
  <div>
    <router-view></router-view>
    <dashboard></dashboard>
  </div>
</template>

<script>
import Dashboard from './layouts/components/Dashboard.vue'

export default {
  components: {
    Dashboard,
  }
}
</script>
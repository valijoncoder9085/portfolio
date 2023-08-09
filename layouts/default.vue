<template>
  <div>
    <SidebarComponents/>
  </div>
</template>

<script>
import SidebarComponents from "~/components/Sidebar.vue";

export default {
  name: 'DefaultLayout',
  components: {SidebarComponents},
  data () {
    return {}
  }
}
</script>
<style lang="scss">
</style>

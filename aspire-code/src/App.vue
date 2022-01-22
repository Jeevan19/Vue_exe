<template>
  <Dashboard />
  <router-view />
</template>
<script>
import { defineComponent } from 'vue';
import { useQuasar } from 'quasar';

export default defineComponent({
  name: 'App',
   setup () {
      // equivalent to calling this on creating the component
    const $q = useQuasar();
    $q.addressbarColor.set('#a2e3fa')
  }
})
</script>

<style lang="scss">
 
</style>

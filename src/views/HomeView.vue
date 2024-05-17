<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/desktop-logo-complet-250x100.svg">
    <CommingSoon msg="Site admin en cours de développement"/>
  </div>
</template>

<script>
// @ is an alias to /src
import CommingSoon from '@/components/CommingSoon.vue';

export default {
  name: 'HomeView',
  components: {
    CommingSoon
  }
}
</script>

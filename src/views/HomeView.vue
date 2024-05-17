<template>
  <div class="home">
    <LogoChanger/>
    <CommingSoon msg="Site admin en cours de développement"/>
  </div>
</template>

<script>
// @ is an alias to /src
import CommingSoon from '@/components/CommingSoon.vue';
import LogoChanger from '@/components/LogoChanger.vue';

export default {
  name: 'HomeView',
  components: {
    CommingSoon,
    LogoChanger
  }
}
</script>

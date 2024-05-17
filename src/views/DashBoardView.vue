<template>
  <div class="home">
    <LogoCommingSoon />
    <DashBoardCommingSoon />
  </div>
</template>

<script>
// @ is an alias to /src
import DashBoardCommingSoon from '@/components/Dashboard/DashBoardCommingSoon.vue';
import LogoCommingSoon from '@/components/LogoCommingSoon.vue';

export default {
  name: 'DashBoardView',
  components: {
    DashBoardCommingSoon,
    LogoCommingSoon
  }
}
</script>
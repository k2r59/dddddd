<template>
  <main>
    <div class="mentions" v-html="mentions" />
  </main>
</template>
<script>
export default {
  name: 'Mentions',
  data() {
    return {
      mentions : window.mentions
    };
  }  
}
</script>
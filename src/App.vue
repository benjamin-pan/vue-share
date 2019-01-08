<template>
  <div id="app">
    <Share :config="config"></Share>
  </div>
</template>

<script>
import Share from './share';

export default {
  name: 'app',
  data() {
    return {
      config: {
      },
    }
  },
  mounted() {},
  components: {
    Share,
  },
}
</script>

<style lang="scss"></style>

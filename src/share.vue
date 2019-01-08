<template>
  <div class="social-share" ref="share"></div>
</template>

<script>
import './js/share.js';

export default {
  name: "Share",
  props: {
    config: {
      type: Object,
      default: {},
    }
  },
  mounted() {
    window.socialShare(this.refs.share, this.config);
  },
}
</script>

<style scoped></style>

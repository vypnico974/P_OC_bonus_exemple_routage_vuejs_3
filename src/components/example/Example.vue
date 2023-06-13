<template>
  <div class="container">
    <p>This is /example</p>
    <div>
      <span>global state count = {{ count }}</span>
    </div>
    <md-button class="md-raised md-primary" @click.native="inc">increase</md-button>
  </div>
</template>

<script>
  export default {
    computed: {
      count () {
        return this.$store.state.count
      }
    },
    methods: {
      inc: function () {
        this.$store.commit('increment')
      }
    }
  }
</script>

<style scoped>
  .container {
    padding: 20px;
  }
</style>

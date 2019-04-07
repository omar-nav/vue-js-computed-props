<template lang = "pug">
  #app
    section.section
      nav.nav.has-shadow 
        .container
          input.input.is-large(type="text", placeholder="buscar canciones")
          a.button.is-info.is-large Buscar
          a.button.is-danger.is-large &times;

      .container
          .columns
            .cloumn
</template>

<script>
export default {
  name: 'app',
  data () {
    return {}
  },
  methods: {
    format () {}
  }
}
</script>

<style lang="scss">
@import "./scss/main.scss";
</style>

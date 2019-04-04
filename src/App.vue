<template lang = "pug">
  #app
    input(v-model="name")
    input(v-model="lastName")
    p {{ fullName }}
    input(v-model="dob" placeholder="year-month-day")
    p {{ age }}
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      name: 'omar',
      lastName: 'cesar',
      dob: '1990-01-01'
    }
  },
  computed: {
    fullName () {
      return this.name + ' ' + this.lastName
    },
    age () {
      let dob = new Date(this.dob)
      let today = new Date()
      let dobYear = dob.getFullYear()
      let todayYear = today.getFullYear()
      let age = todayYear - dobYear
      return age
    }
  }
}
</script>

<style lang="scss">
@import "./scss/main.scss";
</style>

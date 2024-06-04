<template>
    <NavBar></NavBar>
    <FormTournoi></FormTournoi>
  </template>

<script>
import NavBar from '../components/NavBar.vue'
import FormTournoi from '../components/FormTournoi.vue'

export default {
  name: 'CreationT',
  components: {
    NavBar,
    FormTournoi
  }
}
</script>

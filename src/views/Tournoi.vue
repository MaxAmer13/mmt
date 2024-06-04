<template>
    <NavBar></NavBar>
    <h1 class="Title">Tournoi</h1>

        <div class="form">
            <LesTournois></LesTournois>
        </div>
  </template>

<script>
import NavBar from '../components/NavBar.vue'
import LesTournois from '../components/LesTournois.vue'

export default {
  name: 'TouRnoi',
  components: {
    NavBar,
    LesTournois
  }
}
</script>

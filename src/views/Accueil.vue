<template>
    <NavBar></NavBar>
    <div class="profile">
            <h2 class="Title">Mes Tournois</h2>
            <h2 class="Title">Mes participations</h2>
        </div>
        <div class="profile">
            <div class="Allt">
                <MesTournois></MesTournois>
            </div>
            <div class="Allt">
                <MesParticipations></MesParticipations>
            </div>
        </div>
  </template>

<script>
import NavBar from '../components/NavBar.vue'
import MesTournois from '../components/MesTournois.vue'
import MesParticipations from '../components/MesParticipations.vue'

export default {
  name: 'AccueiL',
  components: {
    NavBar,
    MesTournois,
    MesParticipations
  }
}
</script>

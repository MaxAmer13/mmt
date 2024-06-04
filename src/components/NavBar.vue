<template>
        <nav>
            <ul class="nav-links">
                <li class="upward">
                    <router-link to="/accueil">Accueil</router-link>
                </li>
                <li class="upward">
                    <router-link to="/tournoi">Tournoi</router-link>
                </li>
                <li class="upward">
                    <router-link to="/creationt">Créer</router-link>
                </li>
            </ul>
        </nav>
</template>

<script>
import { RouterLink } from 'vue-router'

export default {
  name: 'NavBar',
  props: {

  }
}
</script>

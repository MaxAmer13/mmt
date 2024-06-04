<template>
  <div class="CenterBox">
            <div class="form-container">
                <p class="title">Se connecter</p>
                <form class="form">
                    <input type="text" class="input" placeholder="Email" v-model="identifiant.email">
                    <input type="password" class="input" placeholder="Mot de Passe" v-model="identifiant.mdp">
                    <p class="page-link">
                    </p>
                    <button class="form-btn" @click="connexion">Connexion</button>
                </form>
                <p class="sign-up-label">
                    Aucun compte ? <span class="sign-up-link"><router-link to="/inscription">Inscrivez-vous</router-link></span>
                </p>
            </div>
  </div>
</template>

<script>

import { RouterLink } from 'vue-router'

export default {
  name: 'HomeView',
  components: {
  },
  data(){
    return {
      identifiant: {
        email: '',
        mdp: ''
      }
    }
  },
  methods: {
    connexion(){
      const form = new FormData();

      form.append('email', JSON.stringify(this.identifiant.email));
      form.append('mdp', JSON.stringify(this.identifiant.mdp));

      fetch('http://localhost/mmt/backend/connexion.php', {
        method: 'POST',
        body: form
      })
      .then(response => {
        console.log(response)
      })
      .catch(error => {
        console.error(error)
        alert("Une erreur est survenue lors de l'inscription.")
      })
    }
  }
}
</script>

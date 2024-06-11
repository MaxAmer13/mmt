<template>
    <div class="CenterBox">
      <div class="form-container-inscri">
        <p class="title">S'inscrire</p>
        <form class="form" @submit.prevent="UpdateAccount">
          <div id="noms">
            <input type="text" class="input" placeholder="Prenom" v-model="utilisateur.prenom" />
            <input type="text" class="input" placeholder="Nom" v-model="utilisateur.nom" />
          </div>
          <input type="text" class="input" placeholder="Email" v-model="utilisateur.email" />
          <input type="password" class="input" placeholder="Mot de Passe" v-model="utilisateur.mdp" />
          <input type="password" class="input" placeholder="Confirmer Mot de passe" v-model="utilisateur.confirmMdp" />
          <button class="form-btn" type="submit">Inscription</button>
        </form>
        <p class="sign-up-label">
          Vous avez déjà un compte ? <span class="sign-up-link"><router-link to="/">Connectez-vous</router-link></span>
        </p>
      </div>
    </div>
  </template>

<script>
export default {
  name: 'InscriPtion',
  data () {
    return {
      utilisateur: {
        prenom: '',
        nom: '',
        email: '',
        mdp: '',
        confirmMdp: ''
      }
    }
  },
  methods: {
    UpdateAccount () {
      const form = new FormData()

      form.append('prenom', JSON.stringify(this.utilisateur.prenom))
      form.append('nom', JSON.stringify(this.utilisateur.nom))
      form.append('email', JSON.stringify(this.utilisateur.email))
      form.append('mdp', JSON.stringify(this.utilisateur.mdp))

      if (this.utilisateur.mdp !== this.utilisateur.confirmMdp) {
        alert('Les mots de passe ne correspondent pas.')
        return
      }
      fetch('http://localhost/mmt/backend/InsertUser.php', {
        method: 'POST',
        body: form
      })
        .then(response => {
          console.log(response)
          alert('Inscription réussie!')
        })
        .catch(error => {
          console.error(error)
          alert("Une erreur est survenue lors de l'inscription.")
        })
    }
  }
}
</script>

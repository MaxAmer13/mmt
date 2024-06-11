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
import store from '@/store/store';

export default {
  name: 'HomeView',
  data() {
    return {
      identifiant: {
        email: '',
        mdp: ''
      }
    };
  },
  methods: {
    connexion : async function (){
            let formCo = new FormData();
            formCo.append('email',this.identifiant.email)
            formCo.append('mdp',this.identifiant.mdp)

            const sendDataCo =  await fetch('http://localhost/mmt/backend/connexion.php',{
                method:'POST',
                body:formCo
                
            })
            
           
            const response = await sendDataCo.json()
            
            console.log(response)
            if(response.id){
            
              await this.$router.push('/accueil')
                
              console.log('connexion réussie')
              localStorage.setItem('id',response.id)
            
            } 
                else{
                    
                    await this.$router.push('/')
                }
            }
            
           

        }
};
</script>
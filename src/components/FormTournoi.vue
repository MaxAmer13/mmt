<template>
    <div class="LineCenterBox">
        <div class="Box">
            <h2 class="title">Création de tournoi</h2>
            <form class="form">
                <input type="text" placeholder="Nom du tournoi" class="input" v-model="tournoi.NomTournoi" required/>
                <select class="input" name="listeSports" v-model="tournoi.Sport">
                    <option value="">Choisir un sport</option>
                    <option v-for="sport in sports" :key="sport.id_sport" :value="sport.id_sport">{{ sport.libelsport }}</option>
                </select>
                <button class="btn" @click="AddSport">Ajouter un Sport</button>
                <select class="input" v-model="tournoi.TypeTournoi" required>
                    <option value="">Type de tournoi</option>
                    <option value="Elimination">Elimination</option>
                    <option value="Championnat">Championnat</option>
                </select>
                <input type="text" placeholder="Nombre de Participants" class="input" v-model="tournoi.NbParticipant" required/>
                <input type="date" class="input" v-model="tournoi.dateT" required/>
                <button class="form-btn" @click="UpdateTourn">Créer</button>
            </form>
        </div>
    </div>
</template>

<script>

export default {
  name: 'FormTournoi',
  data () {
    return {
      tournoi: {
        NomTournoi: '',
        Sport: '',
        TypeTournoi: '',
        NbParticipant: 0,
        dateT: ''
      },
      sports:[]
    }
  },
  methods: {
    UpdateTourn () {
      const form = new FormData()

      form.append('nomtournoi', JSON.stringify(this.tournoi.NomTournoi))
      form.append('typetournoi', JSON.stringify(this.tournoi.TypeTournoi))
      form.append('nbParticipant', JSON.stringify(this.tournoi.NbParticipant))
      form.append('date', JSON.stringify(this.tournoi.dateT))
      form.append('sport', JSON.stringify(this.tournoi.Sport))

      fetch('http://localhost/mmt/backend/InsertTournoi.php', {

        method: 'POST',
        body: form
      })
        .then(response => {
          console.log(response)
          alert('Tournoi Ajouté')
        })
        .catch(error => {
          console.error(error)
          alert("Une erreur est survenue lors de l'inscription.")
        })
    }, AddSport(){
        let libelsport = window.prompt('Nom du Sport');
        let formSport = new FormData()

        formSport.append('libelSport', JSON.stringify(libelsport))
        fetch('http://localhost/mmt/backend/InsertSport.php', {
            method: 'POST',
            body: formSport
        })
        .then(response => {
            console.log(this.tournoi.Sport)
            alert('Sport ajouté')
        })
        .catch(error => {
            console.error(error)
            alert("Une erreur est survenue lors de l'ajout du sport.")
        })
    },
    PrintSport(){
        fetch('http://localhost/mmt/backend/AllSport.php', {
        })
        .then(response => response.json())
        .then(data => {
                this.sports = data
            })
        .catch(error => {
            console.error(error)
        })
    }
  },
  mounted(){
        this.PrintSport();
    }
}
</script>

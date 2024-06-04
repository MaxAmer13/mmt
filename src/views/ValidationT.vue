<template>
    <NavBar></NavBar>
    <h1 class="Title">Tournoi de Patrick</h1>
        <div id="apage">
            <div id="commentary">
                <div>
                    <input type="text" class="input" disabled placeholder="Prenom"/>
                    <input type="text" class="input" disabled placeholder="Nom"/>
                </div>
                <textarea placeholder="Commentaire"></textarea>
                <div>
                    <button class="form-btn-green">Accepter</button>
                    <button class="form-btn-red">Refuser</button>
                </div>
            </div>
            <ul class="select">
                <li>Jean pasletemps</li>
                <li>incroyable</li>
                <li>incredible</li>
                <li>De toute façon</li>
            </ul>
        </div>
  </template>

<script>
import NavBar from '../components/NavBar.vue'

export default {
  name: 'ValidationT',
  components: {
    NavBar
  }
}
</script>

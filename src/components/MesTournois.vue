<template>
    <div class="Tournament">
        <label>
            {{ libelTournoi }}
        </label>
        <label> {{ libelSport }}</label>
        <label>0/ {{ nombreparticipant }} </label>
        <button class="form-btn">Voir les participations</button>
    </div>
</template>

<script>
export default {
  name: 'MesTournois',
  props: {
  },methods: {

  }
}
</script>

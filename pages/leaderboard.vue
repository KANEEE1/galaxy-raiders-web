<template>
  <div class="table-container">
    <table>
      <thead>
        <tr>
          <th>Colocação</th>
          <th>Data</th>
          <th>Meteoros Destruídos</th>
          <th>Pontuação</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(game, index) in games" :key="index" :class="index % 2 === 0 ? 'even-row' : 'odd-row'">
<td>{{ index + 1 }}</td>
<td>{{ new Date(game.timestamp).toLocaleDateString() }}</td>
<td>{{ game.asteroidsDestroyed }}</td>
<td>{{ game.finalScore }}</td>
</tr>
</tbody>
</table>
  </div>
</template>
<script>
import data from '../mock-leaderboard.json';

export default {
  data() {
    return {
      games: [],
    };
  },
  mounted() {
    this.games = data.games;
  },
};
</script>
<style scoped>
.table-container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background: url('~/assets/space.gif') no-repeat center center fixed;
  background-size: cover;
  font-size: 2.5em;
}

table {
  width: 80%;  
  height: 80%; 
  border-collapse: separate;
  border-spacing: 0;
  border: 5px solid white; /* sublinhado branco */
  border-radius: 15px;
  overflow: hidden;
  background-color: #0000FF; /* Cor de fundo azul */
}

th, td {
  border: 1px solid #000000; /* Borda branca */
  padding: 12px; 
  text-align: center;
  color: #000000; /* Cor do texto branco */
}

th {
  background-color: #0000FF; /* Cabeçalho azul */
  color: white;
}

tr {
  background-color: #FFFFFF; /* Cor de fundo das linhas pares verde */
}
</style>

<template>
  <div class="menu-container">
    <h1 class="title">Menu</h1>
    <ul class="menu-list">
      <li>
        <nuxt-link to="/game" class="menu-link">Iniciar partida</nuxt-link>
      </li>
      <li>
        <nuxt-link to="/leaderboard" class="menu-link">Placar</nuxt-link>
      </li>
      <li>
        <a href="#" @click.prevent="exitGame" class="menu-link">Sair</a>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  methods: {
    exitGame() {
      window.location.href = 'https://www.youtube.com/watch?v=dQw4w9WgXcQ';
    }
  }
};
</script>

<style>
.menu-container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  height: 100vh;
  background-image: url('~/assets/space.gif');
  background-size: cover;
  background-repeat: no-repeat;
}

.title {
  font-size: 48px;
  color: #fff;
  margin-bottom: 40px;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.2);
}

.menu-list {
  list-style: none;
  padding: 0;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.menu-link {
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 10px;
  padding: 20px;
  width: 200px; /* Largura dos botões */
  font-size: 24px;
  color: #fff;
  background-color: #007bff;
  text-decoration: none;
  border-radius: 5px;
  box-shadow: 0px 2px 4px rgba(0, 0, 0, 0.2);
  transition: background-color 0.3s ease;
}

.menu-link:hover {
  background-color: #0056b3;
  box-shadow: 0px 4px 6px rgba(0, 0, 0, 0.2);
}
</style>

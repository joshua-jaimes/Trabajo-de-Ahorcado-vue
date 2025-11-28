<template>
  <div class="contenedor">
    <h2 class="titulo">Elige una categoría</h2>

    <div class="grid">
      <div
        v-for="cat in categorias"
        :key="cat.texto"
        class="card"
        :style="{ background: cat.color }"
      >
        <span class="emoji">{{ cat.icono }}</span>
        <p>{{ cat.texto }}</p>
        <router-link to="/tercera"></router-link>
      </div>
    </div>
  </div>
</template>

<script setup>
const categorias = [
  { texto: "Frutas", icono: "🍎", color: "linear-gradient(45deg,#ff9a9e,#fad0c4)" },
  { texto: "Animales", icono: "🦁", color: "linear-gradient(45deg,#a1c4fd,#c2e9fb)" },
  { texto: "Países", icono: "🌍", color: "linear-gradient(45deg,#84fab0,#8fd3f4)" },
  { texto: "Deportes", icono: "⚽", color: "linear-gradient(45deg,#f6d365,#fda085)" },
  { texto: "Películas", icono: "🎬", color: "linear-gradient(45deg,#667eea,#764ba2)" },
  { texto: "Ciencia", icono: "🔬", color: "linear-gradient(45deg,#e0c3fc,#8ec5fc)" }
];
</script>

<style scoped>
.contenedor {
  max-width: 950px;
  margin: auto;
  padding: 28px;
  text-align: center;
}

.titulo {
  font-size: 35px;
  margin-bottom: 53px;
  font-weight: bold;
}

.grid {
  display: grid;
  gap: 26px;
  grid-template-columns: repeat(auto-fit, minmax(290px, 1fr));
}

.card {
  padding: 25px;
  border-radius: 18px;
  color: white;
  cursor: pointer;
  transition: 0.2s;
  display: flex;
  flex-direction: column;
  align-items: center;
  font-size: 21px;
}

.card:hover {
  transform: scale(1.05);
}

.emoji {
  font-size: 45px;
  margin-bottom: 10px;
}
</style>

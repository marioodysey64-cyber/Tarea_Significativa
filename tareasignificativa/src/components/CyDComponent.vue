<template>
  <div>
    <h1>Cursos y diplomado por campus</h1>
    <h3>Selecciona la regional de tu interés y te mostraremos los cursos que ofertamos</h3>
    <div class="grid-container">
      <div class="card">
        <img src="https://www.itca.edu.sv/wp-content/uploads/2024/05/La-Union-2.jpg" alt="Curso La Unión" />
        <h4>Campus La Unión</h4>
      </div>
      <div class="card">
        <img src="https://www.itca.edu.sv/wp-content/uploads/2024/06/SanMiguel.jpg" alt="Curso San Miguel" />
        <h4>Campus San Miguel</h4>
      </div>
      <div class="card">
        <img src="https://www.itca.edu.sv/wp-content/uploads/2024/05/Zacatecoluca.jpg" alt="Curso Zacatecoluca" />
        <h4>Campus Zacatecoluca</h4>
      </div>
      <div class="card">
        <img src="https://www.itca.edu.sv/wp-content/uploads/2024/05/Santa-Tecla-2-1.jpg" alt="Curso Santa Tecla" />
        <h4>Campus Santa Tecla</h4>
      </div>
      <div class="card">
        <img src="https://www.itca.edu.sv/wp-content/uploads/2024/05/Santa-Ana.jpg" alt="Curso Santa Ana" />
        <h4>Campus Santa Ana</h4>
      </div>
    </div>
  </div>
</template>

<script setup>
// No se requiere lógica por ahora
</script>

<style scoped>
.grid-container {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(400px, 1fr));
  gap: 16px;
  margin-top: 20px;
}

.card {
  text-align: center;
}

.card img {
  width: 100%;
  height: auto;
  object-fit: cover;
  border-radius: 8px;
  box-shadow: 0 2px 6px rgba(0, 0, 0, 0.1);
}

.card h4 {
  margin-top: 8px;
  font-size: 1.1rem;
  color: #333;
}
  
h1 {
  color: rgb(255, 51, 0);
}
.card img {
  width: 100%;
  height: auto;
  object-fit: cover;
  border-radius: 8px;
  box-shadow: 0 2px 6px rgba(0, 0, 0, 0.1);
  transition: transform 0.3s ease;
}

.card img:hover {
  transform: scale(1.05); /* Aumenta el tamaño en un 5% */
}
</style>
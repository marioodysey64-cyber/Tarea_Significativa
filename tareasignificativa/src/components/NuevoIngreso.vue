<!-- src/components/MenuGrid.vue -->
<template>
  <div class="container">
    <!-- Grid de botones -->
    <main class="grid">
<a
  v-for="btn in gridButtons"
  :key="btn"
  :href="getExternalLink(btn)"
  class="grid-button"
  target="_blank"
  rel="noopener"
>
  {{ btn }}
</a>
<router-link
  v-for="btn in gridbutton"
  :key="btn"
  :to="getRoute(btn)"
  class="grid-button"
>
  {{ btn }}
</router-link>
      <div class="open-house-button">
        <a href='https://forms.office.com/pages/responsepage.aspx?id=qqDrMPJSZ0GUPM8PrFQ4pxCn7ev6fchPkHCsd6hnekBUNU1CWFBQTUkxTlI2TzhQNlJYMVRWOUdETC4u&route=shorturl'> OPEN HOUSE</a>
      </div>
    </main>
  </div>
</template>

<script setup>

const gridButtons = [
  'Requisitos',
  'Brochure',
  'Pasos para inscribirse en línea',
  'Aranceles',
  'Contáctenos',
  'Becas'
]
const gridbutton=[
    'Carreras impartidas'
]
const getExternalLink = (label) => {
  const map = {
    'Brochure': 'https://www.itca.edu.sv/wp-content/uploads/2025/06/Brochure_CE26_2_compressed.pdf',
    'Requisitos': 'https://www.itca.edu.sv/requisitos-inscripcion/',
    'Pasos para inscribirse en línea': 'https://www.itca.edu.sv/pasos-inscripcion/',
    'Aranceles': 'https://www.itca.edu.sv/wp-content/uploads/2025/09/Aranceles_Web2026_compressed.pdf',
    'Contáctenos': 'https://www.itca.edu.sv/inscripcion-contactenos/',
    'Becas': 'https://www.itca.edu.sv/becas/',
    'OPEN HOUSE': 'https://forms.office.com/pages/responsepage.aspx?id=qqDrMPJSZ0GUPM8PrFQ4pxCn7ev6fchPkHCsd6hnekBUNU1CWFBQTUkxTlI2TzhQNlJYMVRWOUdETC4u&route=shorturl'
  }
  return map[label] || '#'
}
const getRoute = (label) => {
  const map = {
    'Carreras Impartidas': '/carreras',
  }
  return map[label] || '/'
}
</script>

<style scoped>
.container {
  display: flex;
  font-family: Arial, sans-serif;
}

/* Grid de botones */
.grid {
  flex: 1;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 10px;
  padding: 1rem;
  align-content: start;
}

.grid-button {
  background-color: #C62828; /* rojo institucional */
  color: white;
  border-color: red;
  padding: 1rem;
  text-align: center;
  font-weight: bold;
  border-radius: 5px;
  cursor: pointer;
}
.grid-button:hover,
.open-house-button:hover {
  background-color: #fffcfc; /* tono más oscuro al pasar el mouse */
  color: red;
  transition: background-color 0.3s ease;
}
.open-house-button {
  grid-column: span 3;
  background-color: #C62828;
  color: white;
  padding: 1.5rem;
  text-align: center;
  font-size: 1.2rem;
  font-weight: bold;
  border-radius: 5px;
  margin-top: 1rem;
}
</style>
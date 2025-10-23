<template>
  <section class="nosotros">
    <!-- Encabezado principal -->
    <div class="nosotros-hero">
      <h1>Sobre Nosotros</h1>
      <p>Formamos técnicos y tecnólogos altamente capacitados, comprometidos con el desarrollo de El Salvador.</p>
    </div>

    <!-- Contenedor principal -->
    <div class="nosotros-container">
      <!-- Columna izquierda -->
      <div class="nosotros-info">
        <h2>Nuestra Misión</h2>
        <p>
          Brindar educación técnica y tecnológica de calidad, promoviendo la innovación, el emprendimiento y la responsabilidad social,
          para contribuir al desarrollo sostenible del país y mejorar la calidad de vida de la sociedad salvadoreña.
        </p>

        <h2>Nuestra Visión</h2>
        <p>
          Ser una institución líder en educación técnica y tecnológica, reconocida a nivel nacional e internacional
          por su excelencia académica y su compromiso con el progreso del país.
        </p>

        <h2>Valores Institucionales</h2>
        <ul>
          <li><strong>Compromiso:</strong> con la formación integral de los estudiantes.</li>
          <li><strong>Excelencia:</strong> en la enseñanza, aprendizaje e innovación.</li>
          <li><strong>Integridad:</strong> en nuestras acciones y relaciones.</li>
          <li><strong>Respeto:</strong> a la diversidad y el pensamiento crítico.</li>
          <li><strong>Trabajo en equipo:</strong> para alcanzar metas comunes.</li>
        </ul>
      </div>

      <!-- Columna derecha -->
      <div class="nosotros-image">
        <img
          src="https://www.itca.edu.sv/wp-content/uploads/2023/05/itca-campus.jpg"
          alt="Campus ITCA-FEPADE"
        />
      </div>
    </div>

    <!-- Sección final -->
    <div class="nosotros-extra">
      <h2>¿Por qué elegir ITCA-FEPADE?</h2>
      <p>
        Porque somos una institución comprometida con la calidad, la innovación y el desarrollo profesional.
        Nuestros programas están diseñados para preparar a los estudiantes con las competencias que demanda el mercado laboral actual.
      </p>
    </div>
  </section>
</template>

<script>
export default {
  name: 'NosotrosComponent',
}
</script>

<style scoped>
.nosotros {
  background-color: #f8f9fa;
  color: #333;
  padding: 60px 20px;
  font-family: "Roboto", sans-serif;
}

/* Encabezado principal */
.nosotros-hero {
  text-align: center;
  margin-bottom: 50px;
}

.nosotros-hero h1 {
  font-size: 2.5rem;
  color: #0c5a8a;
  margin-bottom: 15px;
}

.nosotros-hero p {
  max-width: 700px;
  margin: 0 auto;
  color: #555;
}

/* Contenedor principal */
.nosotros-container {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 40px;
  max-width: 1100px;
  margin: 0 auto 60px;
  align-items: center;
}

.nosotros-info h2 {
  color: #0c5a8a;
  margin-top: 25px;
}

.nosotros-info p {
  line-height: 1.7;
  color: #444;
  margin-bottom: 10px;
}

.nosotros-info ul {
  margin-top: 10px;
  padding-left: 20px;
}

.nosotros-info li {
  margin-bottom: 8px;
  color: #333;
}

.nosotros-image img {
  width: 100%;
  border-radius: 12px;
  box-shadow: 0 6px 16px rgba(0, 0, 0, 0.2);
  transition: transform 0.3s ease;
}

.nosotros-image img:hover {
  transform: scale(1.03);
}

/* Sección final */
.nosotros-extra {
  background-color: #0c5a8a;
  color: white;
  text-align: center;
  padding: 50px 20px;
  border-radius: 10px;
  max-width: 1000px;
  margin: 0 auto;
}

.nosotros-extra h2 {
  margin-bottom: 15px;
}

/* Responsivo */
@media (max-width: 992px) {
  .nosotros-container {
    grid-template-columns: 1fr;
    text-align: center;
  }
  .nosotros-info {
    order: 2;
  }
  .nosotros-image {
    order: 1;
  }
}
</style>

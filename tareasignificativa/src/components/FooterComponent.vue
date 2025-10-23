<template>
  <footer class="footer">
    <div class="footer-container">

      <!-- Columna Izquierda - Acerca de ITCA -->
      <div class="footer-column">
        <h3 class="footer-heading">ACERCA DE ITCA</h3>
        <nav class="footer-nav">
          <a href="#">¿Quiénes somos?</a>
          <a href="#">Misión y Visión</a>
          <a href="#">Carreras</a>
          <a href="#">Sedes</a>
        </nav>
      </div>

      <!-- Columna Central - Logo -->
      <div class="footer-column footer-logo">
        <img
          src="https://www.itca.edu.sv/wp-content/uploads/2025/01/LogoITCA_Web.png"
          alt="ITCA FEPADE"
          class="gobierno-logo"
        />
      </div>

      <!-- Columna Derecha - Enlaces y Redes Sociales -->
      <div class="footer-column footer-links">
        <h3 class="footer-heading">INSTITUCIÓN</h3>
        <nav class="footer-nav">
          <a href="#">Cooperación Nacional e Internacional</a>
          <a href="#">Gestión de la Calidad</a>
          <a href="#">Investigación y Proyección Social</a>
          <a href="#">Publicaciones</a>
          <a href="#">Buzón de Sugerencias, Quejas y Reclamos</a>
        </nav>

        <div class="footer-social">
          <a href="#"><i class="fab fa-facebook-f"></i></a>
          <a href="#"><i class="fab fa-twitter"></i></a>
          <a href="#"><i class="fab fa-instagram"></i></a>
          <a href="#"><i class="fab fa-youtube"></i></a>
        </div>
      </div>

    </div>

    <div class="footer-bottom">
      <p>© 2025 Instituto Tecnológico Centroamericano (ITCA-FEPADE). Todos los derechos reservados.</p>
    </div>
  </footer>
</template>

<script>
export default {
  name: "FooterComponent",
};
</script>

<style scoped>
.footer {
  background-color: #1e1e1e;
  color: #fff;
  padding: 40px 0;
  text-align: center;
}

.footer-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-around;
  align-items: start;
  gap: 30px;
  margin-bottom: 20px;
}

.footer-column {
  flex: 1;
  min-width: 200px;
}

.footer-heading {
  font-size: 1.2em;
  margin-bottom: 15px;
  border-bottom: 2px solid #f4a261;
  display: inline-block;
  padding-bottom: 5px;
}

.footer-nav a {
  display: block;
  color: #ccc;
  text-decoration: none;
  margin: 5px 0;
  transition: color 0.3s;
}

.footer-nav a:hover {
  color: #f4a261;
}

.footer-social a {
  color: #fff;
  margin: 0 10px;
  font-size: 1.3em;
  transition: color 0.3s;
}

.footer-social a:hover {
  color: #f4a261;
}

.footer-logo img {
  width: 150px;
  margin: 10px 0;
}

.footer-bottom {
  border-top: 1px solid #333;
  padding-top: 15px;
  font-size: 0.9em;
  color: #bbb;
}
</style>

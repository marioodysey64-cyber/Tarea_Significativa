<template>
  <nav class="navbar">
    <div class="navbar-top">
      <img
        src="https://www.itca.edu.sv/wp-content/uploads/2025/01/LogoITCA_Web.png"
        alt="Logo"
        class="logo-img"
      />

      <div class="navbar-icons">
        <i class="fab fa-facebook-f"></i>
        <i class="fab fa-instagram"></i>
        <i class="fab fa-youtube"></i>
        <i class="fab fa-tiktok"></i>
        <i class="fab fa-linkedin-in"></i>
        <input type="text" placeholder="Buscar..." class="search-bar" />
        <i class="fas fa-search"></i>
      </div>
    </div>

    <ul class="navbar-menu">
      <li><router-link to="/">Inicio</router-link></li>
      <li><router-link to="/titular">Registro de Titular</router-link></li>
      <li><router-link to="/beneficiario">Registro de Beneficiario</router-link></li>
      <li><router-link to="/cita">Realizar Cita</router-link></li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: "NavBar"
};
</script>

<style scoped>
@import url("https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css");

.navbar {
  width: 100%;
  background: linear-gradient(to bottom, #eac56d, #c79000);
  color: #7a4700;
  font-family: "Segoe UI", sans-serif;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
}

/* --- Top bar --- */
.navbar-top {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 10px 30px;
}

.logo-img {
  height: 60px;
  background: none;
}

.navbar-icons {
  display: flex;
  align-items: center;
  gap: 15px;
  color: #a56b00;
}

.navbar-icons i {
  cursor: pointer;
  transition: transform 0.2s;
}

.navbar-icons i:hover {
  transform: scale(1.2);
  color: #7a4700;
}

.search-bar {
  padding: 5px 10px;
  border-radius: 5px;
  border: none;
  outline: none;
}

/* --- Menu --- */
.navbar-menu {
  display: flex;
  justify-content: center;
  list-style: none;
  margin: 0;
  padding: 10px 0;
  background: linear-gradient(to bottom, #c79000, #b67a00);
}

.navbar-menu li {
  padding: 0 20px;
  border-right: 1px solid rgba(255, 255, 255, 0.2);
}

.navbar-menu li:last-child {
  border-right: none;
}

.navbar-menu a {
  color: white;
  text-decoration: none;
  font-weight: 600;
  text-transform: uppercase;
  font-size: 14px;
  transition: color 0.3s;
}

.navbar-menu a:hover {
  color: #ffe38a;
}

/* Responsive */
@media (max-width: 768px) {
  .navbar-top {
    flex-direction: column;
    gap: 10px;
  }

  .navbar-menu {
    flex-direction: column;
    align-items: center;
  }

  .navbar-menu li {
    border: none;
    padding: 10px 0;
  }
}
</style>

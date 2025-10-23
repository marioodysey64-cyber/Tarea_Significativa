<template>
  <nav class="navbar">
    <div class="navbar-logo">
      <img src="https://pbs.twimg.com/profile_images/1795102790064205824/d99d9de8_400x400.jpg" alt="ISSS" class="logo-img">
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
}
</script>

<style scoped>
.navbar {
  background-color: #005f8f;
  color: white;
  padding: 15px 30px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
}

.navbar-logo {
  display: flex;
  align-items: center;
}

.logo-img {
  height: 50px;
  width: auto;
  object-fit: contain;
  background-color: white;
  padding: 5px 15px;
  border-radius: 5px;
}

.navbar-menu {
  list-style: none;
  display: flex;
  gap: 30px;
  margin: 0;
  padding: 0;
}

.navbar-menu li {
  margin: 0;
}

.navbar-menu a {
  color: white;
  text-decoration: none;
  font-weight: 500;
  font-size: 15px;
  transition: all 0.3s ease;
  padding: 8px 12px;
  border-radius: 5px;
}

.navbar-menu a:hover {
  background-color: rgba(255, 255, 255, 0.1);
  text-decoration: none;
}

.navbar-menu a.router-link-active {
  background-color: rgba(255, 255, 255, 0.2);
  font-weight: 600;
}

/* Responsive */
@media (max-width: 768px) {
  .navbar {
    flex-direction: column;
    gap: 15px;
    padding: 15px;
  }

  .navbar-menu {
    flex-direction: column;
    gap: 10px;
    width: 100%;
    text-align: center;
  }

  .logo-img {
    height: 40px;
  }
}
</style>
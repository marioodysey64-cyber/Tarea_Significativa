<template>
  <div class="home">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'HomeView',
  components: {
    HelloWorld
  }
}
</script>

<style scoped>
.inicio {
  min-height: calc(100vh - 80px);
}

/* Carrusel */
.carousel-container {
  position: relative;
  width: 100%;
  height: 500px;
  overflow: hidden;
}

.carousel {
  width: 100%;
  height: 100%;
}

.carousel-slide {
  position: relative;
  width: 100%;
  height: 100%;
}

.carousel-slide img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.carousel-overlay {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: linear-gradient(to bottom, rgba(0, 0, 0, 0.3), rgba(0, 95, 143, 0.7));
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  color: white;
  text-align: center;
  padding: 40px;
}

.carousel-overlay h1 {
  font-size: 48px;
  margin-bottom: 20px;
  text-shadow: 2px 2px 8px rgba(0, 0, 0, 0.5);
  animation: slideInDown 0.8s ease;
}

.carousel-overlay p {
  font-size: 24px;
  max-width: 800px;
  text-shadow: 1px 1px 4px rgba(0, 0, 0, 0.5);
  animation: slideInUp 0.8s ease;
}

/* Botones del carrusel */
.carousel-btn {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  background-color: rgba(255, 255, 255, 0.3);
  color: white;
  border: none;
  width: 50px;
  height: 50px;
  border-radius: 50%;
  cursor: pointer;
  transition: all 0.3s ease;
  display: flex;
  align-items: center;
  justify-content: center;
  z-index: 10;
}

.carousel-btn:hover {
  background-color: rgba(255, 255, 255, 0.5);
  transform: translateY(-50%) scale(1.1);
}

.carousel-btn.prev {
  left: 20px;
}

.carousel-btn.next {
  right: 20px;
}

/* Indicadores */
.carousel-indicators {
  position: absolute;
  bottom: 20px;
  left: 50%;
  transform: translateX(-50%);
  display: flex;
  gap: 10px;
  z-index: 10;
}

.carousel-indicators button {
  width: 12px;
  height: 12px;
  border-radius: 50%;
  border: 2px solid white;
  background-color: transparent;
  cursor: pointer;
  transition: all 0.3s ease;
}

.carousel-indicators button.active {
  background-color: white;
  transform: scale(1.2);
}

/* Transiciones */
.fade-enter-active, .fade-leave-active {
  transition: opacity 0.5s ease;
}

.fade-enter-from, .fade-leave-to {
  opacity: 0;
}

/* Sección de bienvenida */
.welcome-section {
  padding: 60px 40px;
  background: linear-gradient(135deg, #005f8f 0%, #0c7db5 100%);
  color: white;
  text-align: center;
}

.welcome-content h2 {
  font-size: 36px;
  margin-bottom: 15px;
}

.welcome-content p {
  font-size: 18px;
  opacity: 0.95;
}

/* Sección de servicios */
.services-section {
  padding: 80px 40px;
  background-color: #f5f5f5;
}

.services-section h2 {
  text-align: center;
  font-size: 36px;
  color: #005f8f;
  margin-bottom: 50px;
}

.services-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 30px;
  max-width: 1200px;
  margin: 0 auto;
}

.service-card {
  background: white;
  padding: 40px 30px;
  border-radius: 12px;
  text-align: center;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
  transition: all 0.3s ease;
  text-decoration: none;
  color: inherit;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.service-card:hover {
  transform: translateY(-10px);
  box-shadow: 0 8px 30px rgba(0, 95, 143, 0.2);
}

.service-icon {
  width: 80px;
  height: 80px;
  background: linear-gradient(135deg, #005f8f 0%, #0c7db5 100%);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 20px;
}

.service-icon svg {
  stroke: white;
}

.service-card h3 {
  font-size: 22px;
  color: #005f8f;
  margin-bottom: 15px;
}

.service-card p {
  font-size: 15px;
  color: #666;
  line-height: 1.6;
}

/* Sección de información */
.info-section {
  padding: 80px 40px;
  background-color: white;
}

.info-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 30px;
  max-width: 1200px;
  margin: 0 auto;
}

.info-card {
  background: linear-gradient(135deg, #005f8f 0%, #0c7db5 100%);
  color: white;
  padding: 40px 30px;
  border-radius: 12px;
  text-align: center;
  box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
}

.info-card h3 {
  font-size: 22px;
  margin-bottom: 20px;
}

.info-card p {
  font-size: 15px;
  margin: 10px 0;
  opacity: 0.95;
}

/* Animaciones */
@keyframes slideInDown {
  from {
    opacity: 0;
    transform: translateY(-30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

@keyframes slideInUp {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

/* Responsive */
@media (max-width: 768px) {
  .carousel-container {
    height: 350px;
  }

  .carousel-overlay h1 {
    font-size: 32px;
  }

  .carousel-overlay p {
    font-size: 18px;
  }

  .welcome-content h2 {
    font-size: 28px;
  }

  .services-section h2 {
    font-size: 28px;
  }

  .carousel-btn {
    width: 40px;
    height: 40px;
  }

  .carousel-btn svg {
    width: 24px;
    height: 24px;
  }
}
</style>
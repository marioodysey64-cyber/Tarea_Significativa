<template>
  <div class="inicio">
    <!-- Carrusel de imágenes -->
    <div class="carousel-container">
      <div class="carousel">
        <transition name="fade" mode="out-in">
          <div :key="currentSlide" class="carousel-slide">
            <img :src="slides[currentSlide].image" :alt="slides[currentSlide].title">
            <div class="carousel-overlay">
              <h1>{{ slides[currentSlide].title }}</h1>
              <p>{{ slides[currentSlide].description }}</p>
            </div>
          </div>
        </transition>
      </div>

      <!-- Controles del carrusel -->
      <button class="carousel-btn prev" @click="prevSlide" aria-label="Anterior">
        <svg xmlns="http://www.w3.org/2000/svg" width="30" height="30" fill="none" stroke="currentColor" stroke-width="2">
          <polyline points="15 18 9 12 15 6" />
        </svg>
      </button>
      <button class="carousel-btn next" @click="nextSlide" aria-label="Siguiente">
        <svg xmlns="http://www.w3.org/2000/svg" width="30" height="30" fill="none" stroke="currentColor" stroke-width="2">
          <polyline points="9 18 15 12 9 6" />
        </svg>
      </button>

      <!-- Indicadores -->
      <div class="carousel-indicators">
        <button 
          v-for="(slide, index) in slides" 
          :key="index"
          @click="goToSlide(index)"
          :class="{ active: currentSlide === index }"
        ></button>
      </div>
    </div>

    <!-- 🔻 NUEVA SECCIÓN (basada en tu código de React, convertida a Vue) -->
    <div class="min-h-screen bg-gray-50">
      <!-- Barra de anuncios superior -->
      <div class="bg-red-700 text-white py-3 overflow-hidden">
        <div class="animate-scroll whitespace-nowrap">
          <span class="inline-block px-8">
            YA FORMANDO A MÁS DE MIL MUJERES ELECTRICISTAS EN EL SALVADOR, CON ITCA-FEPADE COMO INSTITUCIÓN FORMADORA
          </span>
          <span class="inline-block px-8">
            LANZAMOS EL PROGRAMA DE EFICIENCIA Y AHORRO ENERGÉTICO
          </span>
          <span class="inline-block px-8">
            YA FORMANDO A MÁS DE MIL MUJERES ELECTRICISTAS EN EL SALVADOR, CON ITCA-FEPADE COMO INSTITUCIÓN FORMADORA
          </span>
        </div>
      </div>

      <!-- Contenido principal -->
      <div class="max-w-7xl mx-auto px-4 py-12">
        <div class="grid md:grid-cols-2 gap-8">
          <!-- Tarjeta Carreras Profesionales -->
          <div class="bg-white rounded-lg shadow-lg overflow-hidden">
            <div class="grid grid-cols-3 gap-1 p-1">
              <div class="col-span-2 row-span-2">
                <img src="https://images.unsplash.com/photo-1581092918056-0c4c3acd3789?w=600&h=600&fit=crop" alt="Estudiantes" class="w-full h-full object-cover" />
              </div>
              <img src="https://images.unsplash.com/photo-1581092160562-40aa08e78837?w=300&h=300&fit=crop" alt="Estudiante 1" class="w-full h-full object-cover" />
              <img src="https://images.unsplash.com/photo-1581092795360-fd1ca04f0952?w=300&h=300&fit=crop" alt="Estudiante 2" class="w-full h-full object-cover" />
              <img src="https://images.unsplash.com/photo-1581092160607-ee22621dd758?w=300&h=300&fit=crop" alt="Estudiante 3" class="w-full h-full object-cover" />
              <img src="https://images.unsplash.com/photo-1581092918484-8313e1f7e8c7?w=300&h=300&fit=crop" alt="Estudiante 4" class="w-full h-full object-cover" />
            </div>
            <div class="p-8 text-center">
              <h2 class="text-3xl font-bold text-gray-800 mb-3">Carreras Profesionales:</h2>
              <p class="text-gray-600 mb-6">Ingenierías y Técnicos.</p>
              <button class="bg-red-700 hover:bg-red-800 text-white font-semibold px-8 py-3 rounded transition-colors duration-300">
                Ver más
              </button>
            </div>
          </div>

          <!-- Tarjeta Cursos y Diplomados -->
          <div class="bg-white rounded-lg shadow-lg overflow-hidden">
            <div class="grid grid-cols-3 gap-1 p-1">
              <img src="https://images.unsplash.com/photo-1556910103-1c02745aae4d?w=300&h=300&fit=crop" alt="Gastronomía" class="w-full h-full object-cover" />
              <img src="https://images.unsplash.com/photo-1454165804606-c3d57bc86b40?w=300&h=300&fit=crop" alt="Diseño" class="w-full h-full object-cover" />
              <img src="https://images.unsplash.com/photo-1581091226825-a6a2a5aee158?w=300&h=300&fit=crop" alt="Electricidad" class="w-full h-full object-cover" />
              <img src="https://images.unsplash.com/photo-1432888622747-4eb9a8f2c293?w=300&h=300&fit=crop" alt="Idiomas" class="w-full h-full object-cover" />
              <img src="https://images.unsplash.com/photo-1581092160562-40aa08e78837?w=300&h=300&fit=crop" alt="Ingeniería" class="w-full h-full object-cover" />
              <img src="https://images.unsplash.com/photo-1517694712202-14dd9538aa97?w=300&h=300&fit=crop" alt="Programación" class="w-full h-full object-cover" />
            </div>
            <div class="p-8 text-center">
              <h2 class="text-3xl font-bold text-gray-800 mb-3">Cursos y Diplomados:</h2>
              <p class="text-gray-600 mb-6">Amplía tus conocimientos con nuestros programas cortos.</p>
              <button class="bg-red-700 hover:bg-red-800 text-white font-semibold px-8 py-3 rounded transition-colors duration-300">
                Ver más
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- 🔺 Fin de la nueva sección -->
  </div>
</template>

<script>
export default {
  name: "InicioView",
  data() {
    return {
      currentSlide: 0,
      autoplayInterval: null,
      slides: [
        {
          image: "https://media.discordapp.net/attachments/854835059764363276/1430942717017329705/image.png",
          title: "CONVIVENCIA",
          description: "Brindamos atención médica de calidad para ti y tu familia",
        },
        {
          image: "https://media.discordapp.net/attachments/854835059764363276/1430942921489911869/image.png",
          title: "Servicios Médicos Especializados",
          description: "Contamos con profesionales altamente capacitados",
        },
        {
          image: "https://media.discordapp.net/attachments/854835059764363276/1430942158252278000/image.png",
          title: "Tecnología de Vanguardia",
          description: "Equipos médicos de última generación para tu atención",
        },
      ],
    };
  },
  mounted() {
    this.startAutoplay();
  },
  beforeUnmount() {
    this.stopAutoplay();
  },
  methods: {
    nextSlide() {
      this.currentSlide = (this.currentSlide + 1) % this.slides.length;
      this.resetAutoplay();
    },
    prevSlide() {
      this.currentSlide = this.currentSlide === 0 ? this.slides.length - 1 : this.currentSlide - 1;
      this.resetAutoplay();
    },
    goToSlide(index) {
      this.currentSlide = index;
      this.resetAutoplay();
    },
    startAutoplay() {
      this.autoplayInterval = setInterval(() => {
        this.nextSlide();
      }, 5000);
    },
    stopAutoplay() {
      clearInterval(this.autoplayInterval);
    },
    resetAutoplay() {
      this.stopAutoplay();
      this.startAutoplay();
    },
  },
};
</script>

<style scoped>
@keyframes scroll {
  0% { transform: translateX(0); }
  100% { transform: translateX(-50%); }
}
.animate-scroll {
  animation: scroll 20s linear infinite;
}
/* Deja aquí tus estilos previos del carrusel y secciones */
</style>

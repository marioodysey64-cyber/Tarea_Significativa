<template>
  <div class="inicio">
    <!-- Carrusel de imágenes -->
    <div class="carousel-container">
      <div class="carousel">
        <transition name="fade" mode="out-in">
          <div :key="currentSlide" class="carousel-slide">
            <img :src="slides[currentSlide].image" :alt="slides[currentSlide].title" />
            <div class="carousel-overlay">
              <h1>{{ slides[currentSlide].title }}</h1>
              <p>{{ slides[currentSlide].description }}</p>
            </div>
          </div>
        </transition>
      </div>

      <!-- Controles del carrusel -->
      <button class="carousel-btn prev" @click="prevSlide" aria-label="Anterior">
        <svg xmlns="http://www.w3.org/2000/svg" width="30" height="30" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
          <polyline points="15 18 9 12 15 6"></polyline>
        </svg>
      </button>
      <button class="carousel-btn next" @click="nextSlide" aria-label="Siguiente">
        <svg xmlns="http://www.w3.org/2000/svg" width="30" height="30" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
          <polyline points="9 18 15 12 9 6"></polyline>
        </svg>
      </button>

      <!-- Indicadores -->
      <div class="carousel-indicators">
        <button 
          v-for="(slide, index) in slides" 
          :key="index"
          @click="goToSlide(index)"
          :class="{ active: currentSlide === index }"
          :aria-label="`Ir a slide ${index + 1}`"
        ></button>
      </div>
    </div>

    <!-- Barra de anuncios superior -->
    <div class="marquee-container">
      <div class="animate-scroll whitespace-nowrap font-bold">
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

    <!-- Contenedor principal de tarjetas -->
    <div class="cards-container max-w-7xl mx-auto px-4 py-12 grid md:grid-cols-2 gap-8">
      <!-- Tarjetas dinámicas desde data -->
      <div v-for="(card, index) in cards" :key="index" class="card bg-white rounded-lg shadow-lg overflow-hidden">
        <div class="card-images grid grid-cols-3 gap-1 p-1">
          <div v-for="(img, i) in card.images" :key="i" :class="img.class">
            <img :src="img.src" :alt="img.alt" class="w-full h-full object-cover" />
          </div>
        </div>
        <div class="p-8 text-center">
          <h2 class="text-3xl font-bold text-gray-800 mb-3">{{ card.title }}</h2>
          <p class="text-gray-600 mb-6">{{ card.description }}</p>
          <button class="bg-red-700 hover:bg-red-800 text-white font-semibold px-8 py-3 rounded transition-colors duration-300">Ver más</button>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'InicioView',
  data() {
    return {
      currentSlide: 0,
      autoplayInterval: null,
      slides: [
        {
          image: 'https://media.discordapp.net/attachments/854835059764363276/1430942717017329705/image.png',
          title: 'CONVIVENCIA',
          description: 'Brindamos atención médica de calidad para ti y tu familia'
        },
        {
          image: 'https://media.discordapp.net/attachments/854835059764363276/1430942921489911869/image.png',
          title: 'Servicios Médicos Especializados',
          description: 'Contamos con profesionales altamente capacitados'
        },
        {
          image: 'https://media.discordapp.net/attachments/854835059764363276/1430942158252278000/image.png',
          title: 'Tecnología de Vanguardia',
          description: 'Equipos médicos de última generación para tu atención'
        },
        {
          image: 'https://media1.tenor.com/m/uSDXgF3E6SUAAAAd/hollow-knight-dance-hollow-knight.gif',
          title: '',
          description: ''
        }
      ],
      cards: [
        {
          title: "Carreras Profesionales",
          description: "Ingenierías y Técnicos.",
          images: [
            { src: "https://images.unsplash.com/photo-1581092918056-0c4c3acd3789?w=600&h=600&fit=crop", alt: "Estudiantes", class: "col-span-2 row-span-2" },
            { src: "https://images.unsplash.com/photo-1581092160562-40aa08e78837?w=300&h=300&fit=crop", alt: "Estudiante 1", class: "" },
            { src: "https://images.unsplash.com/photo-1581092795360-fd1ca04f0952?w=300&h=300&fit=crop", alt: "Estudiante 2", class: "" },
            { src: "https://images.unsplash.com/photo-1581092160607-ee22621dd758?w=300&h=300&fit=crop", alt: "Estudiante 3", class: "" },
            { src: "https://images.unsplash.com/photo-1581092918484-8313e1f7e8c7?w=300&h=300&fit=crop", alt: "Estudiante 4", class: "" }
          ]
        },
        {
          title: "Cursos y Diplomados",
          description: "Amplía tus conocimientos con nuestros programas cortos.",
          images: [
            { src: "https://images.unsplash.com/photo-1556910103-1c02745aae4d?w=300&h=300&fit=crop", alt: "Gastronomía", class: "" },
            { src: "https://images.unsplash.com/photo-1454165804606-c3d57bc86b40?w=300&h=300&fit=crop", alt: "Diseño", class: "" },
            { src: "https://images.unsplash.com/photo-1581091226825-a6a2a5aee158?w=300&h=300&fit=crop", alt: "Electricidad", class: "" },
            { src: "https://images.unsplash.com/photo-1432888622747-4eb9a8f2c293?w=300&h=300&fit=crop", alt: "Idiomas", class: "" },
            { src: "https://images.unsplash.com/photo-1581092160562-40aa08e78837?w=300&h=300&fit=crop", alt: "Ingeniería", class: "" },
            { src: "https://images.unsplash.com/photo-1517694712202-14dd9538aa97?w=300&h=300&fit=crop", alt: "Programación", class: "" }
          ]
        }
      ]
    }
  },
  mounted() { this.startAutoplay() },
  beforeUnmount() { this.stopAutoplay() },
  methods: {
    nextSlide() { this.currentSlide = (this.currentSlide + 1) % this.slides.length; this.resetAutoplay(); },
    prevSlide() { this.currentSlide = this.currentSlide === 0 ? this.slides.length - 1 : this.currentSlide - 1; this.resetAutoplay(); },
    goToSlide(index) { this.currentSlide = index; this.resetAutoplay(); },
    startAutoplay() { this.autoplayInterval = setInterval(() => this.nextSlide(), 5000); },
    stopAutoplay() { if (this.autoplayInterval) clearInterval(this.autoplayInterval); },
    resetAutoplay() { this.stopAutoplay(); this.startAutoplay(); }
  }
}
</script>

<style scoped>
/* Barra de anuncios */
.marquee-container { background-color: #b91c1c; overflow: hidden; }
.animate-scroll { animation: scroll 20s linear infinite; font-weight: bold; color: white; }

/* Carrusel */
.inicio { min-height: calc(100vh - 80px); }
.carousel-container { position: relative; width: 100%; height: 500px; overflow: hidden; }
.carousel { width: 100%; height: 100%; }
.carousel-slide { position: relative; width: 100%; height: 100%; }
.carousel-slide img { width: 100%; height: 100%; object-fit: cover; }
.carousel-overlay { position: absolute; top:0; left:0; right:0; bottom:0; background: linear-gradient(to bottom, rgba(0,0,0,0.3), rgba(0,95,143,0.7)); display:flex; flex-direction: column; justify-content:center; align-items:center; color:white; text-align:center; padding:40px; }
.carousel-overlay h1 { font-size:48px; margin-bottom:20px; text-shadow:2px 2px 8px rgba(0,0,0,0.5); animation:slideInDown 0.8s ease; }
.carousel-overlay p { font-size:24px; max-width:800px; text-shadow:1px 1px 4px rgba(0,0,0,0.5); animation:slideInUp 0.8s ease; }

/* Botones y indicadores */
.carousel-btn { position:absolute; top:50%; transform:translateY(-50%); background-color: rgba(255,255,255,0.3); color:white; border:none; width:50px; height:50px; border-radius:50%; cursor:pointer; display:flex; align-items:center; justify-content:center; z-index:10; transition:all 0.3s ease; }
.carousel-btn:hover { background-color: rgba(255,255,255,0.5); transform:translateY(-50%) scale(1.1); }
.carousel-btn.prev { left:20px; }
.carousel-btn.next { right:20px; }
.carousel-indicators { position:absolute; bottom:20px; left:50%; transform:translateX(-50%); display:flex; gap:10px; z-index:10; }
.carousel-indicators button { width:12px; height:12px; border-radius:50%; border:2px solid white; background-color:transparent; cursor:pointer; transition:all 0.3s ease; }
.carousel-indicators button.active { background-color:white; transform:scale(1.2); }
.fade-enter-active, .fade-leave-active { transition: opacity 0.5s ease; }
.fade-enter-from, .fade-leave-to { opacity:0; }

/* Tarjetas */
.cards-container { gap:2rem; }
.card-images { display:grid; gap:0.25rem; }
.card-images img { width:100%; height:100%; object-fit:cover; }

/* Animaciones */
@keyframes scroll { 0% { transform: translateX(0); } 100% { transform: translateX(-50%); } }
@keyframes slideInDown { from { opacity:0; transform: translateY(-30px); } to { opacity:1; transform: translateY(0); } }
@keyframes slideInUp { from { opacity:0; transform: translateY(30px); } to { opacity:1; transform: translateY(0); } }

/* Responsive */
@media (max-width:768px) {
  .carousel-container { height:350px; }
  .carousel-overlay h1 { font-size:32px; }
  .carousel-overlay p { font-size:18px; }
  .carousel-btn { width:40px; height:40px; }
  .carousel-btn svg { width:24px; height:24px; }
}
</style>

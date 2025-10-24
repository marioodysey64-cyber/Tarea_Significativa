<template>
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

    <!-- Contenedor principal -->
    <div class="max-w-7xl mx-auto px-4 py-12">
      <div class="grid md:grid-cols-2 gap-8">
        <!-- Tarjeta Carreras Profesionales -->
        <div class="bg-white rounded-lg shadow-lg overflow-hidden">
          <!-- Grid de imágenes -->
          <div class="grid grid-cols-3 gap-1 p-1">
            <div class="col-span-2 row-span-2">
              <img 
                src="https://images.unsplash.com/photo-1581092918056-0c4c3acd3789?w=600&h=600&fit=crop" 
                alt="Estudiantes" 
                class="w-full h-full object-cover"
              />
            </div>
            <div>
              <img 
                src="https://images.unsplash.com/photo-1581092160562-40aa08e78837?w=300&h=300&fit=crop" 
                alt="Estudiante 1" 
                class="w-full h-full object-cover"
              />
            </div>
            <div>
              <img 
                src="https://images.unsplash.com/photo-1581092795360-fd1ca04f0952?w=300&h=300&fit=crop" 
                alt="Estudiante 2" 
                class="w-full h-full object-cover"
              />
            </div>
            <div>
              <img 
                src="https://images.unsplash.com/photo-1581092160607-ee22621dd758?w=300&h=300&fit=crop" 
                alt="Estudiante 3" 
                class="w-full h-full object-cover"
              />
            </div>
            <div>
              <img 
                src="https://images.unsplash.com/photo-1581092918484-8313e1f7e8c7?w=300&h=300&fit=crop" 
                alt="Estudiante 4" 
                class="w-full h-full object-cover"
              />
            </div>
          </div>

          <!-- Contenido de la tarjeta -->
          <div class="p-8 text-center">
            <h2 class="text-3xl font-bold text-gray-800 mb-3">
              Carreras Profesionales:
            </h2>
            <p class="text-gray-600 mb-6">
              Ingenierías y Técnicos.
            </p>
            <button class="bg-red-700 hover:bg-red-800 text-white font-semibold px-8 py-3 rounded transition-colors duration-300">
              Ver más
            </button>
          </div>
        </div>

        <!-- Tarjeta Cursos y Diplomados -->
        <div class="bg-white rounded-lg shadow-lg overflow-hidden">
          <!-- Grid de imágenes -->
          <div class="grid grid-cols-3 gap-1 p-1">
            <div>
              <img 
                src="https://images.unsplash.com/photo-1556910103-1c02745aae4d?w=300&h=300&fit=crop" 
                alt="Gastronomía" 
                class="w-full h-full object-cover"
              />
            </div>
            <div>
              <img 
                src="https://images.unsplash.com/photo-1454165804606-c3d57bc86b40?w=300&h=300&fit=crop" 
                alt="Diseño" 
                class="w-full h-full object-cover"
              />
            </div>
            <div>
              <img 
                src="https://images.unsplash.com/photo-1581091226825-a6a2a5aee158?w=300&h=300&fit=crop" 
                alt="Electricidad" 
                class="w-full h-full object-cover"
              />
            </div>
            <div>
              <img 
                src="https://images.unsplash.com/photo-1432888622747-4eb9a8f2c293?w=300&h=300&fit=crop" 
                alt="Idiomas" 
                class="w-full h-full object-cover"
              />
            </div>
            <div>
              <img 
                src="https://images.unsplash.com/photo-1581092160562-40aa08e78837?w=300&h=300&fit=crop" 
                alt="Ingeniería" 
                class="w-full h-full object-cover"
              />
            </div>
            <div>
              <img 
                src="https://images.unsplash.com/photo-1517694712202-14dd9538aa97?w=300&h=300&fit=crop" 
                alt="Programación" 
                class="w-full h-full object-cover"
              />
            </div>
          </div>

          <!-- Contenido de la tarjeta -->
          <div class="p-8 text-center">
            <h2 class="text-3xl font-bold text-gray-800 mb-3">
              Cursos y Diplomados:
            </h2>
            <p class="text-gray-600 mb-6">
              Amplia tus conocimientos con nuestros programas cortos.
            </p>
            <button class="bg-red-700 hover:bg-red-800 text-white font-semibold px-8 py-3 rounded transition-colors duration-300">
              Ver más
            </button>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "CursosComponent",
};
</script>

<style scoped>
@keyframes scroll {
  0% {
    transform: translateX(0);
  }
  100% {
    transform: translateX(-50%);
  }
}

.animate-scroll {
  animation: scroll 20s linear infinite;
}
</style>

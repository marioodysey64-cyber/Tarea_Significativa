<template>
  <v-footer app color="teal-darken-4" dark>
    <v-container>
      <v-row>
        <!-- Sección Recursos Estudiantiles -->
        <v-col cols="12" md="4">
          <h3 class="text-h6 mb-2">Recursos Estudiantiles</h3>
          <v-list density="compact" bg-color="transparent">
            <v-list-item
              v-for="(item, i) in recursos"
              :key="i"
              :href="item.link"
              target="_blank"
              prepend-icon="mdi-school"
            >
              <v-list-item-title>{{ item.titulo }}</v-list-item-title>
            </v-list-item>
          </v-list>
        </v-col>

        <!-- Sección Información institucional -->
        <v-col cols="12" md="4">
          <h3 class="text-h6 mb-2">ITCA-FEPADE</h3>
          <p>
            Formación técnica y tecnológica de calidad.<br />
            San Salvador, El Salvador.
          </p>
        </v-col>

        <!-- Redes sociales -->
        <v-col cols="12" md="4" class="text-center">
          <h3 class="text-h6 mb-2">Síguenos</h3>
          <v-btn
            v-for="(icon, i) in redes"
            :key="i"
            :icon="icon.name"
            :href="icon.link"
            target="_blank"
            class="mx-1"
            color="white"
            variant="text"
          ></v-btn>
        </v-col>
      </v-row>

      <v-divider class="my-3"></v-divider>

      <div class="text-center text-caption">
        © {{ new Date().getFullYear() }} ITCA-FEPADE — Todos los derechos reservados
      </div>
    </v-container>
  </v-footer>
</template>

<script>
export default {
  name: 'FooterITCA',
  data() {
    return {
      recursos: [
        { titulo: 'Biblioteca Virtual', link: 'https://biblioteca.itca.edu.sv' },
        { titulo: 'Plataforma Moodle', link: 'https://moodle.itca.edu.sv' },
        { titulo: 'Correo Institucional', link: 'https://mail.google.com/a/itca.edu.sv' },
        { titulo: 'Calendario Académico', link: '#' },
      ],
      redes: [
        { name: 'mdi-facebook', link: 'https://facebook.com/itcafepade' },
        { name: 'mdi-instagram', link: 'https://instagram.com/itcafepade' },
        { name: 'mdi-youtube', link: 'https://youtube.com/@itcafepade' },
      ],
    }
  },
}
</script>

<style scoped>
p {
  color: #e0f2f1;
}
</style>

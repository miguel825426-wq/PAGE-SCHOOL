<template>
       <v-toolbar class="text-white" image="https://images.pexels.com/photos/159751/book-address-book-learning-learn-159751.jpeg?cs=srgb&dl=pexels-pixabay-159751.jpg&fm=jpg"
     height="100">

      <v-toolbar-title text="INSTITUCIÓN EDUCATIVA SANTOS ABREIRO"></v-toolbar-title>

      <v-btn icon="mdi-export"></v-btn>
    </v-toolbar>
  <v-app id="inspire">

    <<v-navigation-drawer
        expand-on-hover
        permanent
        rail
      >
        <v-list>
          <v-list-item
            prepend-avatar="https://randomuser.me/api/portraits/women/85.jpg"

            title="I.E SANTOS ABREIRO"
          ></v-list-item>
        </v-list>

        <v-divider></v-divider>

        <v-list density="compact" nav>
          <v-list-item prepend-icon="mdi-folder" title="Registro" value="myfiles" to="/dashboard/registro/"></v-list-item>
          <v-list-item prepend-icon="mdi-account-multiple" title="Matricula" value="shared" to="/dashboard/matricula/"></v-list-item>
          <v-list-item prepend-icon="mdi-star" title="Salir" value="starred" to="/"></v-list-item>
          <v-list-item prepend-icon="mdi-star" title="Asignaturas" value="starred" ></v-list-item>

        </v-list>
      </v-navigation-drawer>
    <v-main>
      <v-container
        class="py-8 px-6"
        fluid
      >
           <router-view />

      </v-container>
    </v-main>
  </v-app>
</template>

<script setup>
  import { ref } from 'vue'

  const cards = ['Today', 'Yesterday']
  const links = [
    ['mdi-inbox-arrow-down', 'Inbox'],
    ['mdi-send', 'Send'],
    ['mdi-delete', 'Trash'],
    ['mdi-alert-octagon', 'Spam'],
  ]

  const drawer = ref(null)
</script>

<script>
  export default {
    data: () => ({
      cards: ['Today', 'Yesterday'],
      drawer: null,
      links: [
        ['mdi-inbox-arrow-down', 'Inbox'],
        ['mdi-send', 'Send'],
        ['mdi-delete', 'Trash'],
        ['mdi-alert-octagon', 'Spam'],
      ],
    }),
  }
</script>
<template>
  <v-card class="overflow-hidden">
    <v-app-bar      
      color="#6A76AB"
      dark     
      shrink-on-scroll
      prominent
      src="./assets/banner.jpg"
      fade-img-on-scroll
      scroll-target="#scrolling-techniques-3"
    >
    <v-img src="./assets/logo.png" style="max-width:200px"></v-img>
      
       
    

      <v-toolbar-title>Seu Shopping de Imóveis</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-heart</v-icon>
      </v-btn>

      <v-btn icon>
        <v-icon>mdi-dots-vertical</v-icon>
      </v-btn>

      <template v-slot:extension>
           <v-hover v-slot:default="{ hover }">
        <v-tabs align-with-title>
          
          <v-tab color="red">Home</v-tab>
          <v-tab>Campanhas</v-tab>
          <v-tab>Geração de Inovadores</v-tab>
          <v-tab>Nossa História</v-tab>
          

          <v-expand-transition>
          <div
            v-if="hover"
            class="d-flex transition-fast-in-fast-out orange darken-2 v-card--reveal display-3 white--text"
            style="height: 100%;"
          >
            
          </div>
        </v-expand-transition>
       
        </v-tabs>
            </v-hover>
  
      </template>
    </v-app-bar>   
     <Body />
     <Footer />
    
  </v-card>
 
</template>

<script>
import Body from './components/Body'
import Footer from './components/Footer'



export default {
  name: 'App',

  components: {
    Body,
    Footer

  },

  data: () => ({
    //
  }),
};
</script>

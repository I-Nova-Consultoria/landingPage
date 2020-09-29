<template>
<v-app>
    <v-card
    max-width="555"
    style="margin-left:50%;"
  >
   

    <v-container>
      <v-row dense>
        <v-col cols="12">
          <v-card
            color="#385F73"
            dark
          >             
           
          </v-card>
        </v-col>

        <v-col
          v-for="(item, i) in items"
          :key="i"
          cols="12"
        >
        <v-hover>
          <v-card
            :color="item.color"
            dark
              :elevation="hover ? 12 : 2"
              :class="{ 'on-hover': hover }"
          >
            <div class="d-flex justify-space-between" style="">
              <div>
                <v-card-title
                  class=""
                  v-text="item.title"
                  style="margin-left:25%;color:black; font-size:20px;white-space: nowrap;"
                ></v-card-title>

                <v-card-subtitle style="margin-left:25%;color:black;" v-text="item.price"></v-card-subtitle>
                <v-card-subtitle  style="margin-left:25%;color:black;" v-text="item.status"></v-card-subtitle>
                <v-card-subtitle style="margin-left:25%;color:black" v-text="item.Realiza"></v-card-subtitle>

              
              </div>

              <v-avatar
                class="ma-3"
                size="120"
                tile
                style="margin-top:-40%;margin-left:2%"
              >
                <v-img :src="item.src"></v-img>
              </v-avatar>
              <v-btn style="position:absolute;margin-left:56%;margin-top:25%;">Faça uma simulação <v-icon>mdi-office-building-marker</v-icon></v-btn>
            </div>
          </v-card>
        </v-hover>
        </v-col>
         <v-form style="background-color:azure;width:600px;height:400px; position:absolute;margin-bottom:80%;margin-left:-130%;">

           <v-container>
          <v-card-title>Construtora:</v-card-title>
           <v-btn color="primary">MRV</v-btn>
           <v-btn color="primary">Tenda</v-btn>
           </v-container>
           <v-container>
          <v-card-title>Faixa de Preço:</v-card-title>
           <v-btn color="primary">80.000 - 120.000</v-btn>
           <v-btn color="primary">120.000 - 160.000</v-btn>
           <v-btn color="primary">Acima de 160.000</v-btn>
           </v-container>
           <v-container>
          <v-card-title>Bairro:</v-card-title>           
           <v-btn color="primary">Centro</v-btn>
           <v-btn color="primary">Recreio</v-btn>
           <v-btn color="primary">Barra da Tijuca</v-btn>
           <v-btn color="primary">Ipanema</v-btn>
           </v-container>

   </v-form>
      </v-row>
      



    </v-container>
  </v-card>
</v-app>
</template>

<script>


  export default {
    data: () => ({
      items: [
        {
          color: '#E5F5FE',
          src: require('../assets/avatar/AP1.jpeg'),
          title: 'Torres no Méier',
          price: '216 Mil',
          Status: 'Status: Lançamento',
          Realiza: 'Construtora: MRV',
        },
        {
          color: '#E5F5FE',
          src: require('../assets/avatar/H1.jpg'),
          title: 'Residencial Tupi',
          price: '182 Mil',
          Status: 'Status: Lançamento',
          Realiza: 'Construtora: MRV',
        },
        {
          color: '#E5F5FE',
          src: require('../assets/avatar/AP2.jpg'),
          title: 'Kitnetes Botafogo',
          price: '200 Mil',
          Status: 'Status: Lançamento',
          Realiza: 'Construtora: MRV',
        },
        {
          color: '#E5F5FE',
          src: require('../assets/avatar/H2.jpeg'),
          title: 'Cobertura Ipanema',
          price: '96 Mil',
          Status: 'Status: Lançamento',
          Realiza: 'Construtora: MRV',
        },
      ],
      methods: {
          //
       }
      
    }),
  }
</script>
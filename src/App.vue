<template>
  <v-app>
    <v-container fluid class="bg">
      <v-row>
        <v-col cols="12" class="">
          <v-row>
            <v-col cols="6">
              <div class="icons">
                <img src="./assets/facebook.svg" alt="" class="social">
                <img src="./assets/instagram.svg" alt="" class="social">
                <img src="./assets/gorjeo.svg" alt="" class="social">
                <a href="https://github.com/VENF"><img src="./assets/github.svg" alt="" class="social"></a>
              </div>
            </v-col>
            <v-col cols="6" class="">
              <div class="nav" v-if="switch1 === false">

                <v-dialog v-model="dialog" persistent max-width="290">
                  <template v-slot:activator="{ on }">
                    <v-btn color="secondary" text class="mx-3" dark v-on="on">About Us</v-btn>
                  </template>
                  <v-card>
                    <v-card-title class="headline">Our company</v-card-title>
                    <v-card-text>
                      Lorem Ipsum is simply dummy text of 
                      the printing and typesetting industry. 
                      Lorem Ipsum has been the industrys standard dummy 
                      text ever since the 1500s, 
                      when an unknown printer took a galley 
                    </v-card-text>
                    <v-card-actions>
                      <v-spacer></v-spacer>
                      <v-btn color="primary" text @click="dialog = false">Cerrar</v-btn>
                    </v-card-actions>
                  </v-card>
                </v-dialog>

                <v-btn color="primary"  class="mx-3">Products</v-btn>

                <v-dialog v-model="dialog2" persistent max-width="290">
                  <template v-slot:activator="{ on }">
                    <v-btn color="secondary" text class="mx-3" dark v-on="on">Contact Us</v-btn>
                  </template>
                  <v-card>
                    <v-card-text>
                      <v-container>
                        <v-text-field label="Email"  outlined></v-text-field>
                          <v-textarea filled auto-grow label="Message" rows="4" row-height="30" shaped></v-textarea>
                          <v-btn color="primary" block elevation="0">Send</v-btn>
                      </v-container>
                    </v-card-text>
                    <v-card-actions>
                      <v-spacer></v-spacer>
                      <v-btn color="primary" text @click="dialog2 = false">Cerrar</v-btn>
                    </v-card-actions>
                  </v-card>
                </v-dialog>

                <v-switch v-model="switch1" :label="`language: ${language}`"></v-switch>
              </div>
              <div class="nav" v-if="switch1 === true">
                <v-dialog v-model="dialog" persistent max-width="290">
                  <template v-slot:activator="{ on }">
                    <v-btn color="secondary" text class="mx-3" dark v-on="on">Nosotros</v-btn>
                  </template>
                  <v-card>
                    <v-card-title class="headline">Nuestra Empresa</v-card-title>
                    <v-card-text>
                      Lorem Ipsum es simplemente un texto ficticio de 
                      la industria de impresión y composición tipográfica. 
                      Lorem Ipsum ha sido el texto ficticio estándar de la 
                    </v-card-text>
                    <v-card-actions>
                      <v-spacer></v-spacer>
                      <v-btn color="primary" text @click="dialog = false">Cerrar</v-btn>
                    </v-card-actions>
                  </v-card>
                </v-dialog>
                <v-btn color="primary" class="mx-3">Productos</v-btn>

                <v-dialog v-model="dialog2" persistent max-width="290">
                  <template v-slot:activator="{ on }">
                    <v-btn color="secondary" text class="mx-3" dark v-on="on">Contactanos</v-btn>
                  </template>
                  <v-card>
                    <v-card-text>
                      <v-container>
                        <v-text-field label="Correo"  outlined></v-text-field>
                          <v-textarea filled auto-grow label="Mensaje" rows="4" row-height="30" shaped></v-textarea>
                          <v-btn color="primary" block elevation="0">Enviar</v-btn>
                      </v-container>
                    </v-card-text>
                    <v-card-actions>
                      <v-spacer></v-spacer>
                      <v-btn color="primary" text @click="dialog2 = false">Cerrar</v-btn>
                    </v-card-actions>
                  </v-card>
                </v-dialog>

                <v-switch v-model="switch1" :label="`language: ${language}`"></v-switch>
              </div>
            </v-col>
          </v-row>
        </v-col>
        <v-col cols="12" class="">
          <v-row class="content-center">
            <v-col cols="12" md="4" class="" v-if="switch1 === false">
              <v-container class="">
                <div class="form">
                  <div class="fields">
                    <v-text-field label="Name"  outlined></v-text-field>
                  </div>
                  <div class="fields">
                    <v-text-field label=" Last Name"  outlined></v-text-field>
                  </div>
                </div>
                <div class="email">
                  <v-text-field label="E-Mail"  outlined></v-text-field>
                </div>
                <v-btn color="primary" block elevation="0">Suscribe!</v-btn>
                <div class="text my-5 text-center">
                  <p class="text-muted">
                    Lorem Ipsum is simply dummy text of 
                    the printing and typesetting industry. 
                    Lorem Ipsum has been the industrys standard dummy 
                    text ever since the 1500s, 
                    when an unknown printer took a galley 
                    of type and scrambled it to make a type specimen book. It has
                  </p>
                </div>
              </v-container>
            </v-col>

            <v-col cols="12" md="4" class="" v-if="switch1 === true">
              <v-container class="">
                <div class="form">
                  <div class="fields">
                    <v-text-field label="Nombre"  outlined></v-text-field>
                  </div>
                  <div class="fields">
                    <v-text-field label="Apellido"  outlined></v-text-field>
                  </div>
                </div>
                <div class="email">
                  <v-text-field label="Correo"  outlined></v-text-field>
                </div>
                <v-btn color="primary" block elevation="0">Suscribete!</v-btn>
                <div class="text my-5 text-center">
                  <p>
                    Lorem Ipsum es simplemente un texto ficticio de 
                    la industria de impresión y composición tipográfica. 
                    Lorem Ipsum ha sido el texto ficticio estándar de la 
                    industria desde el año 1500, 
                    cuando una impresora desconocida tomó una galera de 
                    tipo y la mezcló para hacer un libro de muestras. Tiene
                  </p>
                </div>
              </v-container>
            </v-col>

            <v-col cols="12" md="8" class="phon">
              <img src="./assets/phon.svg" alt="" class="svg">
            </v-col>
          </v-row>
        </v-col>
      </v-row>
      <v-row class="bg-2">
        <v-col cols="12" class="products">
          <products></products>
        </v-col>
      </v-row>
    </v-container>
  </v-app>
</template>

<style scoped>
  .bg{
    background: url('./assets/fondo.svg') no-repeat center;
    background-size: cover;
    height: 100vh;
  }
  .bg-2{
    background: url('./assets/fondo2.svg') no-repeat center;
    background-size: cover;
    height: 100vh;
  }
  .content-center{
    height: 80vh;
  }
  .phon{
    display: grid;
    align-content: center;
    justify-content: center;
    padding-right: 15em;
  }
  .svg{
    height: 100%;
  }
  .nav{
    display: grid;
    grid-template-columns: repeat(5, 1fr);
  }
  .icons{
    display: grid;
    grid-template-columns: repeat(4, 1fr)
  }
  .social{
    height: 20px;
  }
  .form{
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 0.5em;
  }
  .products{
    display: grid;
    align-items: center;
    justify-items: center;
  }
  @media(max-width: 940px){
    .nav{
      display: grid;
      grid-template-columns: 1fr 1fr;
      grid-template-rows: 1fr 1fr;
    }
  }
</style>

<script>
import products from './components/Products.vue';
export default {
  name: 'App',
  components: {
    products
  },
  watch: {
     switch1: function(){
       if(this.switch1 === true){
        this.language = 'Español';
       }else{
         this.language = 'English'
       }
     }
  },
  data: () => ({
    switch1: false,
    language: 'English',
    dialog: false,
    dialog2: false,
  }),
};
</script>

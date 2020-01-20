<template>
  <v-container class="products-content" fluid>
    <v-hover v-slot:default="{ hover }" v-for="item of items" :key="item.id">
      <v-card class="" color="grey lighten-4 mx-3 my-2" max-width="300">
        <v-img :aspect-ratio="16/9"  src="../assets/img2.jpg" >
          <v-expand-transition>
            <div v-if="hover" class="d-flex transition-fast-in-fast-out bg-landing darken-2 v-card--reveal display-3 white--text" style="height: 100%;">
              {{ item.price }}
            </div>
          </v-expand-transition>
        </v-img>
        <v-card-text class="pt-6" style="position: relative;">
          <v-btn absolute color="primary" class="white--text" fab large righ top>
            <v-icon>mdi-cart</v-icon>
          </v-btn>
          <div class="font-weight-light grey--text title mb-2"> {{item.headerTitle}} </div>
          <h3 class="display-1 font-weight-light color-landing mb-2"> {{ item.title }} </h3>
          <div class="font-weight-light title mb-2">
            {{ item.text }}
          </div>
        </v-card-text>
      </v-card>
    </v-hover>
  </v-container>  
</template>

<style>
.color-landing{
  color: #7437DF;
}
.bg-landing{
  background: #7437DF;
}
.v-card--reveal {
  align-items: center;
  bottom: 0;
  justify-content: center;
  opacity: .5;
  position: absolute;
  width: 100%;
}
.products-content{
  display: grid;
  grid-template-columns: repeat(4, 1fr)
}
  @media(max-width: 1350px){
    .products-content{
      display: grid;
      grid-template-columns: 1fr 1fr;
      grid-template-rows: 1fr 1fr;
    }
  }
  @media(max-width: 550px){
    .products-content{
      display: grid;
      grid-template-columns: 1fr;
      justify-items: center;
    }
  }
</style>

<script>
export default {
    name: 'Products',
    data() {
      return {
        items: [
          {
           headerTitle: 'Lorem Ipsum is simply', title: 'the printing and typesettin', text: 'Lorem Ipsum has been the industrys standard dummy, Lorem Ipsum has been the industrys standard dummy', price: 14.99
          },
          {
          headerTitle: 'Lorem Ipsum is simply', title: 'the printing and typesettin', text: 'Lorem Ipsum has been the industrys standard dummy, Lorem Ipsum has been the industrys standard dummy', price: 10.99,
          },
          {
          headerTitle: 'Lorem Ipsum is simply', title: 'the printing and typesettin', text: 'Lorem Ipsum has been the industrys standard dummy, Lorem Ipsum has been the industrys standard dummy', price: 8.99
          },
          {
          headerTitle: 'Lorem Ipsum is simply', title: 'the printing and typesettin', text: 'Lorem Ipsum has been the industrys standard dummy, Lorem Ipsum has been the industrys standard dummy', price: 18.99
          }
        ]
      }
    },
}
</script>
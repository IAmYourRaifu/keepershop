<template>
  <v-app>
  <v-carousel>
    <v-carousel-item
        v-for="(item,i) in items"
        :key="i"
        :src="item.src"
        reverse-transition="fade-transition"
        transition="fade-transition"
    ></v-carousel-item>
  </v-carousel>
    <v-card
        max-width="100%"
        class="mx-auto"
        style="margin-top: 80px; box-shadow: none; margin-bottom:10px"
    >
      <v-container class="pa-1">
        <v-item-group
            v-model="selected"
            multiple
        >
          <v-row>
            <v-col
                v-for="(item2, i) in items2"
                :key="i"
                cols="12"
                md="2"
            >
              <v-item v-slot="{ active, toggle }">
                <v-img
                    :src="`https://static.wikia.nocookie.net/bindingofisaacre_gamepedia/images/${item2.src}`"
                    height="320"
                    class="text-right pa-2"
                    @click="toggle"
                >

                  <v-btn
                      icon
                      dark
                  >
                    <v-icon>
                      {{ active ? 'mdi-heart' : 'mdi-heart-outline' }}
                    </v-icon>
                  </v-btn>
                </v-img>

              </v-item>
              <p style="text-align: center; margin-top: 10px;">{{item2.name}}</p>
            </v-col>
          </v-row>
        </v-item-group>
      </v-container>
    </v-card>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      items: [
        {
          src: 'https://i.pinimg.com/originals/73/2d/ae/732daeefd747c609a7af8a9c068985ed.jpg',
        },
        {
          src: 'https://i.redd.it/n7axrt2bzp351.png',
        },
        {
          src: 'https://i.redd.it/n3al861xzug01.png',
        },
        {
          src: 'https://i.redd.it/84a2skcy4e201.png',
        },
      ],
      items2: [
        {
          src: '7/75/Collectible_The_Bible_icon.png',
          name: 'The Bible',
        },
        {
          src: '3/3e/Collectible_Glass_Cannon_icon.png',
          name: 'Glass Cannon',
        },
        {
          src: 'e/ee/Collectible_Ceremonial_Robes_icon.png',
          name: 'Ceremonial Robes',
        },
        {
          src: '4/47/Collectible_Death%27s_Touch_icon.png',
          name: 'Death Touch',
        },
        {
          src: 'a/a8/Collectible_Epic_Fetus_icon.png',
          name: 'Epic Fetus',
        },
        {
          src: '4/48/Collectible_Goat_Head_icon.png',
          name: 'Goat Head',
        },
        {
          src: '2/2a/Collectible_Holy_Mantle_icon.png',
          name: 'Holy Mantle',
        },
        {
          src: '1/13/Collectible_Ipecac_icon.png',
          name: 'Ipecac',
        },
        {
          src: 'f/fc/Collectible_Spindown_Dice_icon.png',
          name: 'Spindown Dice',
        },
        {
          src: '7/79/Collectible_Mom%27s_Knife_icon.png',
          name: 'Mom Knife',
        },
        {
          src: '3/3b/Collectible_Technology_Zero_icon.png',
          name: 'Technology',
        },
        {
          src: '6/62/Collectible_TMTRAINER_icon.png',
          name: 'ZZaZZ ZZdZZiZZmZZhZZ ZZvZZ ZZoZZ ZZ ZZsZZlZZhZZsZZoZZaZZiZZ',
        },
      ],
      selected: []
    }
  },
}
</script>

<style>
.pa-1{
  background-color: green !important;
}
body{
  background-color: green !important;
}
 #app, body, .theme--light, .v-card, .v-pagination__item--active{
   background-color: green !important;
 }
</style>
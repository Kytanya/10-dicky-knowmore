<template>
  <v-container class="pt-15">
      <v-row>
          <v-col lg="6">
              <h2 class="intro-text">The Land of Rising Sun</h2>
              <p class="description">Japan is known as the “Land of Rising Sun”.
                   It is called by this name because the sun rises first in Japan and then in any other part of the world.</p>
                <v-btn color="#6ea6f1" class="white--text mr-5" rounded>Let's Learn</v-btn>
                <v-btn color="#6ea6f1" class="white--text" rounded><v-icon>mdi-cast-variant</v-icon></v-btn>
          </v-col>
          <v-col lg="6">
              <img width="600" src="./../assets/Jepang.jpg" alt="">
          </v-col>
      </v-row>
  </v-container>
</template>

<script>
export default {
    name:"App",
    data(){
        return{
            menus:[
        {title:'Home',route:'home'},
        {title:'About Us',route:'about-us'},
        {title:'Protofolio',route:'protofolio'},
        {title:'Project',route:'project'},
        {title:'Gallery',route:'gallery'},
        {title:'Contact Us',route:'contact'},
      ]
        }
    }

}
</script>

<style scoped>
h2.intro-text {
    font-size: 60px;
    font-family: Poppins;
    font-weight: semibold;
     color: #0F0F0F;
}

p.description {
    font-size: 15px;
    font-family: Poppins;
    font-weight: semibold;
    margin: 25px 0px;
    color: #0F0F0F;
}

.v-toolbar__title {
    font-size: 1.25rem;
    line-height: 1.5;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
    font-family: Poppins;
    font-weight: bold;
    color: #0F0F0F;
}
</style>
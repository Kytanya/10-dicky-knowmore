<template>
  <v-app-bar
      app
      color="white"
      light
      elevation="5"
      elevate-on-scroll
    >
    <v-toolbar-title>Knowmore</v-toolbar-title>
     <v-spacer />
    <v-list class="d-flex align-center">
      <v-list-item link v-for="(menu,index) in menus" :key="index" :to="menu.route">
        <v-list-item-title>{{menu.title}}</v-list-item-title>
      </v-list-item>
      <v-btn text>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>
      <v-btn color="#6ea6f1" class=white--text rounded>Begin Your Journey</v-btn>
    </v-list>
    </v-app-bar>
</template>

<script>
export default {
    name:"App",
data(){
    return{
        menus:[
        {title:'Home',route:'home'},
        {title:'About Me',route:'about-me'},
        {title:'Gallery',route:'gallery'},
        {title:'Contact Us',route:'contact'},
      ]
    }    
}
};

</script>

<style scoped>
.v-list-item__title {
    font-family: poppins;
    font-weight: semibold;
    font-size: 15px;
     color: #0F0F0F;
}
</style>
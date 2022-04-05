<template>
  <v-app>
    <Header/>
    <v-main>
<HeroComponent/>
<Gallery />
<Contactus />
<Footer/>
    </v-main>
  </v-app>
</template>

<script>
import Header from './components/Header.vue';
import HeroComponent from './components/HeroComponent.vue';
import Gallery from './components/Gallery.vue';
import Contactus from './components/Contactus.vue';
import Footer from './components/Footer.vue';

export default {
  components: { Header, HeroComponent, Gallery, Contactus , Footer},
 name: 'App',
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

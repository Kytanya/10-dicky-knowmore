<template>
  <v-footer
    light
    padless
  >
    <v-card
      flat
      tile
      class="grey darken-3 white--text text-center"
    >
      <v-card-text>
        <v-btn
          v-for="icon in icons"
          :key="icon"
          class="mx-4 white--text"
          icon
        >
          <v-icon size="24px">
            {{ icon }}
          </v-icon>
        </v-btn>
      </v-card-text>

      <v-card-text class="white--text pt-0">
Ki Ora!, My name is Kytanya, Many people think this is my ingame name even though it is, But Kytanya itself comes from my own name, I have several hobbies that people consider normal, I like to Editing something, But i sometimes feel bored because of Editing

I often spend my time playing Games with my Friends, I only leave my home when I need to, Besides for saving money, I also save energy, I love japan culture, All about Japanese, Like Game , Movie, Anime, Song and even more, Okay ill hope everyone have a wonderful day, Alright Sayonara Mate!
      </v-card-text>

      <v-divider></v-divider>

      <v-card-text class="white--text">
        {{ new Date().getFullYear() }} — <strong>Kytanya</strong>
      </v-card-text>
    </v-card>
  </v-footer>
</template>

<script>
export default {
    name:"App",
    data(){
        return{
        icons: [
        'mdi-youtube',
        'mdi-instagram',
        'mdi-twitch',
      ],

        }
    }

}
</script>

<style>

</style>
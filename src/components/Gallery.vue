<template>
  <v-container class="my-15">
      <v-row justify="center">
          <v-col lg="12" class="text-center">
              <v-subheader class="text-h4 justify-center">Take A Look</v-subheader>
              <p>Japan have a such a really nice views you will missed out if you are not visiting</p>
        </v-col>  
        <v-col lg="12">
            <div class="text-center">
                <v-chip @click="activeGallery = 'tokyo'" :color="activeGallery === 'tokyo'? '#6ea6f1':''" class="mx-5 white--text">Tokyo</v-chip>
                <v-chip @click="activeGallery = 'kyoto'" :color="activeGallery === 'kyoto'? '#6ea6f1':''" class="mx-5 white--text">Kyoto</v-chip>
                <v-chip @click="activeGallery = 'osaka'" :color="activeGallery === 'osaka'? '#6ea6f1':''" class="mx-5 white--text">Osaka</v-chip>
            </div>
              </v-col >
            <slot v-if="activeGallery === 'tokyo'">
                <v-col lg="3" v-for="(tokyo,tokyoindex) in tokyo" :key="tokyoindex">
<v-card>
            <v-img
              :src="tokyo.image"
              class="white--text align-end"
              gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
              height="200px"
            >
              <v-card-title>{{tokyo.title}}</v-card-title>
            </v-img>
          </v-card> 
        </v-col></slot>
        
                    <slot v-if="activeGallery === 'kyoto'">
                <v-col lg="3" v-for="(kyoto,kyotoindex) in kyoto" :key="kyotoindex">
<v-card>
            <v-img
              :src="kyoto.image"
              class="white--text align-end"
              gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
              height="200px"
            >
              <v-card-title>{{kyoto.title}}</v-card-title>
            </v-img>
          </v-card> 
        </v-col></slot>

        <slot v-if="activeGallery === 'osaka'">
                <v-col lg="3" v-for="(osaka,osakaindex) in osaka" :key="osakaindex">
<v-card>
            <v-img
              :src="osaka.image"
              class="white--text align-end"
              gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
              height="200px"
            >
              <v-card-title>{{osaka.title}}</v-card-title>
            </v-img>
          </v-card> 
        </v-col></slot>
      </v-row>
  </v-container>
</template>

<script>
export default {
    name:"App",
    data(){
        return{
            activeGallery:'tokyo',
            tokyo:[
                {title:'Tsukiji Outer Market',image:'https://rimage.gnst.jp/livejapan.com/public/article/detail/a/00/01/a0001773/img/en/a0001773_parts_5e3299ceef927.jpg?20201222155112&q=80'},
                {title:'Imperial Palace Area',image:'https://rimage.gnst.jp/livejapan.com/public/article/detail/a/00/01/a0001773/img/en/a0001773_parts_5a5da0ea78984.jpg?20201222155112&q=80'},
                {title:'Akihabara',image:'https://rimage.gnst.jp/livejapan.com/public/article/detail/a/00/01/a0001773/img/en/a0001773_parts_5a5da130d6057.jpg?20201222155112&q=80'},
                
            ],
            kyoto:[
                {title:'Nijo Castle',image:'https://www.planetware.com/photos-large/JPN/japan-kyoto-nijo-castle.jpg'},
                {title:'Kinkaku-ji',image: 'https://www.planetware.com/photos-large/JPN/japan-kyoto-kinkaku-ji-golden-pavilion.jpg'},
                {title:'Kiyomizu-dera Temple',image:'https://www.planetware.com/wpimages/2020/09/japan-kyoto-top-attractions-kiyomizu-dera-temple.jpg'},
            ],
            osaka:[
                {title:'Universal Studios',image:'https://www.japan-guide.com/thumb/238/XYZeXYZe4021_375.jpg'},
                {title:'Osaka Aquarium',image: 'https://www.japan-guide.com/thumb/238/XYZeXYZe4004_375.jpg'},
                {title:'Minami (Namba)',image:'https://www.japan-guide.com/thumb/238/XYZeXYZe4001_375.jpg'},
            ]
            
        }
    }

}
</script>

<style scoped>
.v-subheader.text-h4.justify-center.theme--light {
    font-family: Poppins;
    font-weight: bold;
    color:#0F0F0F;
}
p {
  font-family: Poppins;
    font-weight: semibold;
    color:#0F0F0F;
}

</style>
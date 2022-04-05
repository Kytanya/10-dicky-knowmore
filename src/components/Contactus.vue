<template>
    <v-container class="my-15">
        <v-row justify="center">
            <v-col lg="12" class="text-center">
            <v-subheader class="text-h4 justify-center">Contact Us</v-subheader>
            <p>Incase you need more touch with us, Just contact us in easily way</p>
            </v-col>

            <v-col lg="6">
                <iframe src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d126438.28548094176!2d112.56174241362163!3d-7.978639465299347!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x2dd62822063dc2fb%3A0x78879446481a4da2!2sMalang%2C%20Malang%20City%2C%20East%20Java!5e0!3m2!1sen!2sid!4v1649177547075!5m2!1sen!2sid" width="550" height="450" style="border:0;" allowfullscreen="" loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>

            </v-col>
            <v-col lg="6">
             <v-form
    ref="form">
    <v-text-field
      v-model="contactInfo.name"
      :counter="10"
      label="Name"
      required
    ></v-text-field>

    <v-text-field
      v-model="contactInfo.email"
      label="E-mail"
      required
    ></v-text-field> 
    <v-textarea label="Message" v-model="contactInfo.message"
    :counter="1500">
    
    </v-textarea>

    <v-btn color="#6ea6f1" class="mr-4 white--text"
      
    >
      Send
    </v-btn>
  </v-form>    
            </v-col> 
        </v-row>
    </v-container>

</template>

<script>
export default {
    name:"App",
    data(){
        return{
           contactInfo:{
               
           }
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
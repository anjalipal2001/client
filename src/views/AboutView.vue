<template>
  <v-container>
  <h1>About</h1>
  
  <p>This app allow the user to add the name of the books and their learnings from that book so they do not highlight their books with image attached to it</p>
<!-- 
footer -->
<v-footer app bottom fixed padless>
  <v-card class="flex" flat tile>
    <v-card-title class="teal lighten-1">
     
      <strong class="subheading"> By Anjali Pal</strong>

      <v-spacer></v-spacer>

      <v-btn v-for="icon in icons" :key="icon" class="mx-4" dark icon>
        <v-icon size="24px">
          {{ icon }}
        </v-icon>
      </v-btn>
    </v-card-title>

    <v-card-text class="py-2 white--text text-center">
      {{ new Date().getFullYear() }} — <strong>By Anjali Pal</strong>
    </v-card-text>
  </v-card>
</v-footer>




</v-container>
</template>
<script>
export default {
  data: () => ({
    icons: [
    
      'mdi-twitter',
      'mdi-linkedin',
      
    ],
  }),
}
</script>

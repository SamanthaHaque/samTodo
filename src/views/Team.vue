<template>
  <div class="team">
    <h1 class="subheading grey--text">Team</h1>

    <v-container class="my-5">

      <v-layout row wrap  style="backgeound-color:#777 !important">
        <v-flex xs12 sm6 md4 lg3 v-for="person in team" :key="person.name">
          <v-card text class="text-center ma-2">
            <v-responsive class="pt-4">
              <v-avatar size="100" class="grey lighten-2">
                <img :src="person.avatar">
              </v-avatar>
            </v-responsive>
            <v-card-text>
              <div class="subheading">{{ person.name }}</div>
              <div class="grey--text">{{ person.role }}</div>
            </v-card-text>
            <v-card-actions style="text-align:center">
              <v-btn text center color="grey">
                <v-icon small >message</v-icon>
                <span class="">Message</span>
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-flex>
      </v-layout>

    </v-container>
    
  </div>
</template>

<script>
export default {
  data() {
    return {
      team: [
        { name: 'Samantha Haque', role: 'Front End Developer', avatar: '/avatar-1.jpg' },
        { name: 'Will Smith', role: 'Graphic designer', avatar: '/avatar-2.jpg' },
        { name: 'Jessica Parker', role: 'Web developer', avatar: '/avatar-3.jpg' },
        { name: 'John Tory', role: 'Social media maverick', avatar: '/avatar-4.jpg' },
        { name: 'Ryan Raynolds', role: 'Sales guru', avatar: '/avatar-5.jpg'}

      ]
    }
  }
}
</script>
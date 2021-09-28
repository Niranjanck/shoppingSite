<template>
  <div>
    <v-card elevation="2" height="60px" width="fill width">
      <v-card-title>
        shop
        <v-spacer></v-spacer>
        <v-btn icon class="nav-btn" color="red"
          ><v-icon>mdi-account</v-icon></v-btn
        >
        <v-btn icon class="nav-btn" color="red"
          ><v-icon>mdi-cart</v-icon></v-btn
        >
        <v-btn icon class="nav-btn" color="red"
          ><v-icon>mdi-heart</v-icon></v-btn
        >
      </v-card-title>
    </v-card>
    <v-divider></v-divider>
  </div>
</template>
<style scoped>
.nav-btn {
  margin-left: 20px;
}
</style>

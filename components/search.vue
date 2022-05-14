<template>
  <v-menu right :offset-y="offset">
    <template v-slot:activator="{ on, attrs }">
      <v-btn color="primary" dark v-bind="attrs" v-on="on"> Dropdown </v-btn>
    </template>
    <v-text-field label="Search..."></v-text-field>
  </v-menu>
</template>

<script>
export default {}
</script>

<style></style>

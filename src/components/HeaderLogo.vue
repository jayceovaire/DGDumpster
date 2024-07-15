<script setup>

</script>

<template>
  <v-img
      class="logo"
      :width="600"
      aspect-ratio="16/9"
    src="../assets/DGD_Color.png"
    cover
    ></v-img>

</template>

<style scoped>

.logo {
  margin-top: 10%;
  margin-bottom: 10%;
}

@media screen and (max-width: 480px) {

  .logo {
    margin-bottom: 40%;
  }


}


</style>
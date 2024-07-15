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
  margin-bottom: 10%;
}

@media screen and (max-width: 480px) {

  .logo {
    margin-top: 30%;
    margin-bottom: 30%;
  }


}


</style>
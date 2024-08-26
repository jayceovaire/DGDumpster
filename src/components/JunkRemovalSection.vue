<script setup>

</script>

<template>


  <v-img
      class="junkRemovalImage"
      src="../assets/junkPhoto.jpg"
      width="50%"
      height="auto"
      max-width="800"
      max-height="1500"
  />

  <div id="junkRemoval" class="junkRemoval">
    <h1>Junk Removal</h1>
    <p>
      We want to make disposing of unwanted items and the task of clean outs more convenient for you by
      providing the labor and equipment for proper disposal. Anywhere from single items to complete home or garage cleanouts,
      residential or commercial. A "you call it and we haul it" service.
    </p>
  </div>
</template>

<style scoped>
.junkRemoval {
  margin-right: 10%;
  margin-left: 10%;
  padding-top: 20%;
  padding-bottom: 5%;
}

.junkRemoval h1 {
  font-size: xxx-large;
}

.junkRemoval p {
  color: white;
}

a {
  color: #68bd46;
  text-decoration: none;
}




/* Media Query for smaller screens */
@media screen and (max-width: 480px) {
  .junkRemoval p,
  .junkRemoval h1 {
    font-size: large; /* Adjust font size smaller for smaller screens */
  }
  .junkRemoval h1 {
    font-size: xx-large;
  }


}
</style>
<script setup>

</script>

<template>
  <h1 class="heroHeader">About Us</h1>
  <div class="hero">
    <v-img
        class="heroImage"
        src="../assets/dgfriends.jpg"
        width="50%"
        height="auto"
        max-width="800"
        max-height="1500"
    />
    <p class="heroText">
      D&G Dumpsters was established in August 2019 by two childhood friends that grew up in New Haven, Michigan.
      We are a locally owned dumpster rental company that is now offering <a href="#junkRemoval">junk removal services</a> as well!
      We service Macomb, St.Clair, Oakland and Wayne counties. We offer 10, 15, and 20 yard dumpsters that are driveway friendly!
      <br> <br>As a small company, we understand the value of getting the best and fairest price. We pride ourselves
      on offering <a href="#dCostLabel">competitive rates</a> without compromising quality or service. We strive to provide you with solutions that meet your needs
      and exceed your expectations, all at a price that feels right. By choosing us, you're not only supporting a local business
      but also benefiting from personalized attention and dedication that larger companies often overlook.
    </p>
  </div>
</template>

<style scoped>
a {
  color: #68bd46;
  text-decoration: none;
}

.heroHeader {
  margin-top: 20%;
  margin-bottom: 2%;
  font-size: xxx-large;
}

.hero {
  margin-right: 10%;
  margin-left: 10%;
  padding-bottom: 20%;
  display: flex;
  flex-direction: row;
  align-items: flex-start; /* Align items at the start to keep them in line */
}

.heroImage {
  margin-right: 2%; /* Add some space between the image and the text */
}

.heroText {
  color: white;
  flex: 1; /* Allow the text to take up the remaining space */
}

/* Media Query for smaller screens */
@media screen and (max-width: 480px) {
  .hero {
    flex-direction: column;
    align-items: center;

  }

  .heroImage {
    width: 100%;
    max-width: none;
    margin-bottom: 2%;
  }

  .heroText {
    font-size: large;
  }
}

@media screen and (max-width: 1720px) {
  .hero {
    flex-direction: column;
    align-items: center;
  }

  .heroImage {
    width: 100%;
    max-height: 50%;
    max-width: none;
    margin-bottom: 2%;
  }
}
</style>
